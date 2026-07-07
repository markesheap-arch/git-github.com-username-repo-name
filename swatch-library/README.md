# Swatch Library

This folder is the source-of-truth starter kit for a reusable Shopify swatch library.

## Files

- `swatch-tracker.csv`: canonical swatch records.
- `variant-swatch-mapping.csv`: maps Shopify product variants to swatches.
- `shopify-fabric-swatch-metaobject.schema.json`: proposed Shopify metaobject definition.
- `images/`: starter swatch image assets referenced by the tracker.

## Recommended Model

Use Shopify metaobjects for reusable swatches instead of duplicating swatch data on every product.

Metaobject type:

```text
fabric_swatch
```

Each swatch should have:

- Display name
- Shopify handle
- Color family
- Hex color
- Material
- Pattern
- Texture image
- Vendor/source collection
- Active flag
- Notes

Products or variants should reference the relevant `fabric_swatch` metaobject. The storefront can then render either the texture image or the hex color from the referenced swatch.

## Image Convention

Use square swatch images, ideally at least `1200x1200`.

The current `images/` files are starter placeholders so product imports and theme work have stable file references. Replace them with real photographed fabric/material assets before publishing customer-facing swatches.

Recommended filename:

```text
swatch-{material}-{color}-{swatch_id}.jpg
```

Example:

```text
swatch-boucle-ivory-sw_0001.jpg
```

## Import Flow

1. Add each new material/color to `swatch-tracker.csv`.
2. Upload matching swatch images to Shopify Files.
3. Create or update Shopify `fabric_swatch` metaobjects from the tracker.
4. Fill `variant-swatch-mapping.csv` with product handles, variant SKUs, and swatch IDs.
5. During product import, attach the variant metafield reference to the correct swatch metaobject.

## Suggested Variant Metafield

Namespace:

```text
custom
```

Key:

```text
swatch
```

Type:

```text
metaobject_reference
```

Reference type:

```text
fabric_swatch
```
