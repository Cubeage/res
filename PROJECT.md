# Cubeage Res

Cubeage Res is a small resource/catalog repository for Cubeage application metadata. It currently owns the `apps.json` catalog that lists app identity, icon, and app-store links.

Lifecycle: `active`
Layer: `other`

## Goals

- Maintain the Cubeage app metadata catalog in a clear repository boundary.
- Keep app identifiers, store URLs, and icon references reviewable in source control.
- Prevent resource metadata from becoming product-specific application logic.

## Non-Goals

- This repository does not own the apps listed in the catalog, their store submissions, or their runtime behavior.
- This repository does not own central CI runner, enterprise release bot, platform preview, or deployment behavior.
- This repository must not become a shared dumping ground for feature flags, secrets, or service-specific configuration.

## Boundaries

The machine-readable source of truth is [.doctrine/project.json](.doctrine/project.json). Agents must treat this repository as a metadata/catalog boundary only.

## Public Surfaces

- App metadata catalog in `apps.json`.

## Delivery

Catalog changes require syntax validation and a consumer smoke check when a consuming application or service is known. Source revert is normally sufficient before consumers ingest the change; after consumption, recovery must account for downstream cache or release behavior.
