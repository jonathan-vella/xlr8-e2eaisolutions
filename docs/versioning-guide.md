---
layout: default
title: Documentation Versioning Guide
nav_exclude: true
permalink: /versioning-guide/
version: 1.1.0
last_updated: 2025-06-12
tags: [documentation, versioning, changelog]
---

# Documentation Versioning Guide

This guide explains how versioning works in the XLR8 E2E Azure AI Solutions documentation site.

## Version Information

Each document in this site contains version information in the YAML front matter:

```yaml
---
layout: default
title: Example Document
version: 1.1.0
last_updated: 2025-06-12
---
```

## Changelog Files

We maintain changelog files at multiple levels:

1. **Main Changelog**: Located at the root of the repository (`/CHANGELOG.md`)
2. **Challenge-specific Changelogs**: Located in each challenge folder:
   - `/docs/01-aiready/CHANGELOG.md`
   - `/docs/02-agent/CHANGELOG.md`
   - `/docs/03-aihub/CHANGELOG.md`

## Versioning Scheme

We follow [Semantic Versioning](https://semver.org/):

- **MAJOR** version for incompatible changes (e.g., 1.0.0 → 2.0.0)
- **MINOR** version for new functionality in a backward-compatible manner (e.g., 1.0.0 → 1.1.0)
- **PATCH** version for backward-compatible bug fixes (e.g., 1.1.0 → 1.1.1)

## Last Updated Date

The `last_updated` field in the front matter shows when a document was last modified. This helps users understand how current the information is.

## Finding Version Information

To find the version information for any document:

1. Look at the top of the page for version and last updated information
2. Check the relevant CHANGELOG.md file for detailed changes
3. Review the main CHANGELOG.md for major version updates
