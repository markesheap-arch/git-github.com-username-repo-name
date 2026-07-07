# Replit Library Recovery Index

Source: pasted Replit Library/task transcript captured in Codex on 2026-07-07.

This file records Replit-side work that is not fully indexed in this local project yet.

## Library Apps

| Replit Library item | Type | Local status | Notes |
|---|---|---|---|
| Bespoken Environments | Website | Missing locally | Likely the environment API/app referenced by Drive docs. |
| Bespoken OS Core | Website | Missing locally | Core operating interface; should be exported or connected before local work continues. |

## Library Documents

| Replit Library item | Type | Local status | Notes |
|---|---|---|---|
| Bespoken Singles Catalog (draft for review) | Spreadsheet | Missing locally | Needs export/copy if it differs from Drive catalog sheets. |
| Bespoken Catalog - Designer-Matched with Supplier Flags | Spreadsheet | Missing locally | Needs export/copy; likely important for product verification and Jim recommendations. |
| Bespoken Catalog - Real Products (singles only) | Spreadsheet | Missing locally | Missing from Drive search; high priority export. |

## Library Images

| Replit Library item | Type | Local status | Notes |
|---|---|---|---|
| Luxurious moody interior design | Image | Missing locally | Export if used as site, campaign, or Jim card imagery. |
| Private atelier studio space | Image | Missing locally | Export if used as brand/site imagery. |
| generated_image | Image | Missing locally | Multiple generated images listed; rename on export. |
| cargo net cascade column | Image | Missing locally | Product image candidate for Cargo Net collection. |
| cargo net single drop pendant | Image | Missing locally | Product image candidate for Cargo Net collection. |
| cargo net enclosed cylinder | Image | Missing locally | Product image candidate for Cargo Net collection. |
| cargo net floating cloud | Image | Missing locally | Product image candidate for Cargo Net collection. |
| cargo net wall sconce | Image | Missing locally | Product image candidate for Cargo Net collection. |
| serenade halo steel hero | Image | Missing locally | Serenade drapery hero image. |
| serenade heritage room | Image | Missing locally | Serenade room/environment image. |
| serenade drapery detail | Image | Missing locally | Swatch/detail image candidate. |
| serenade olive collection | Image | Missing locally | Serenade collection image. |
| serenade collector relief | Image | Missing locally | Collector/relief image candidate. |

## Confirmed Replit Task: Jim Catalog Expansion

Task title:

```text
#6 - Give Jim a wider catalog so more room questions get real picks
```

Goal:

Jim previously recommended from an 8-product curated catalog. The Replit task broadened the catalog so more room/category prompts return product cards instead of advice-only responses.

Confirmed task requirements from transcript:

- Add real products across more rooms/categories:
  - bedroom
  - dining
  - entryway
  - kids' rooms
  - outdoor
  - storage
  - dining chairs
  - side tables
  - mirrors
  - poufs
  - throws
- Preserve the Serenade drapery naming lock.
- Preserve Bespoken branding.
- Extend:

```text
artifacts/api-server/src/scripts/seed-shopify-catalog.ts
```

- Generate product imagery into:

```text
artifacts/bespoken-storefront/public/images/catalog/
```

- Publish to all Shopify publications, including the `Replit` channel.
- Follow publishing notes in:

```text
.agents/memory/shopify-catalog-seed.md
```

## Replit Agent Work Log Summary

The Replit Agent transcript states:

- Read existing catalog seeding and Jim recommendation files.
- Read the media-generation skill.
- Edited `seed-shopify-catalog.ts`.
- Generated 16 new product images.
- Typecheck produced pre-existing unrelated route-file errors; the seed script was not among them.
- Seeder initially timed out but created products.
- A second run confirmed and re-published all products.
- Storefront API verification succeeded.
- End-to-end keyword/category checks showed every room/category now had matching products.
- Rebase conflict was resolved by keeping both additive blocks.
- Post-merge setup succeeded.
- Final attempt to re-run seeder after merge failed because:

```text
The ability to use Replit Agent has been disabled by your admin.
```

## Files Changed In Replit Commit

The pasted transcript references a separate Replit commit:

```text
Make Green Street live on the community map with new houses and trees
```

Changed files:

```text
artifacts/mockup-sandbox/src/components/mockups/community-map/CommunityMap.tsx
attached_assets/screenshots/24678808-077a-4397-be66-767266c6d3a2-00-1mte4fljkgfi5_spock_replit_dev_mockup_preview_community-map_CommunityMap.png
docs/bespoken-org-registry.md
```

Commit intent:

- Replace `Verdant Walk` with `Green Street`.
- Add houses, trees, and lamps.
- Update registry documentation with live status, curator, and pending collection name.

## Missing Exports To Request From Replit

High priority:

1. `Bespoken Catalog - Real Products (singles only)`
2. `Bespoken Catalog - Designer-Matched with Supplier Flags`
3. `Bespoken Singles Catalog (draft for review)`
4. Product image folder:

```text
artifacts/bespoken-storefront/public/images/catalog/
```

5. Updated seeder:

```text
artifacts/api-server/src/scripts/seed-shopify-catalog.ts
```

6. Jim recommendation/catalog grounding files.
7. `Bespoken Environments` export or repo snapshot.
8. `Bespoken OS Core` export or repo snapshot.

Image assets to export:

- Cargo Net product images
- Serenade hero/detail/collection images
- Generated interior/studio images

## Local Follow-Up Plan

1. Import or paste the three Replit catalog spreadsheets.
2. Normalize them into local CSVs under `catalog/`.
3. Copy Replit-generated product images into `assets/catalog/`.
4. Reconcile the real-product catalog against Drive's Private Label Furniture working sheet.
5. Extend the local swatch library with Serenade and fabric-specific rows once the image assets arrive.
6. If app code is exported, inspect Jim's catalog grounding path before modifying any Shopify seed data locally.
