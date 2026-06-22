# Repository Instructions

Follow the enterprise doctrine in `SylphxAI/doctrine` and the local project boundary in [PROJECT.md](PROJECT.md). The machine-readable control-plane manifest is [.doctrine/project.json](.doctrine/project.json).

This repository owns resource/catalog metadata only. Do not add application runtime behavior, secrets, feature flags, central CI, release-bot, or platform-preview behavior here.

For catalog changes, validate the catalog syntax and record consumer evidence when the consuming project is known.
