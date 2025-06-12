---
layout: default
title: Documentation Standards
nav_exclude: true
version: 1.1.0
last_updated: 2025-06-12
tags: [documentation, standards, guidelines]
---

# Documentation Standards

This document outlines the standardized naming conventions and documentation structure for the IFS AI Challenges.

## Table of Contents
{:.no_toc}

* TOC
{:toc}

## File Naming Conventions

All challenge files follow a consistent naming pattern:

### Challenge Main Files
- Main challenge pages: `ai-ready-challenge.md`, `ai-agent-challenge.md`, `ai-hub-challenge.md`

## Frontmatter Requirements

All documentation files should include the following frontmatter:

```yaml
---
layout: default
title: Document Title
parent: Parent Page (if applicable)
nav_order: X
tags: [tag1, tag2, tag3]
version: 1.1.0
last_updated: YYYY-MM-DD
---
```

### Required Fields
- **layout**: Usually "default" unless a specific layout is needed
- **title**: Clear, descriptive title of the page
- **nav_order**: Numeric order in the navigation menu
- **tags**: Array of relevant keywords for searching and filtering
- **version**: Document version following semantic versioning (MAJOR.MINOR.PATCH)
- **last_updated**: Date of last update in YYYY-MM-DD format

### Optional Fields
- **parent**: Parent page for hierarchical navigation
- **has_children**: Set to "true" for pages with child pages
- **permalink**: Custom URL path for the page
- Each in repository root for easy navigation

### Challenge-Specific Files

Files are organized in numbered directories by challenge:
- Challenge 1: `01-aiready/`
- Challenge 2: `02-agent/`
- Challenge 3: `03-aihub/`

### Standard File Naming Pattern

Files within each challenge directory follow this pattern:
```
ifs-{challenge}-{content-type}.md
```

Where:
- `{challenge}` is one of: `ready`, `agent`, or `aihub`
- `{content-type}` is one of:
  - `overview` - Challenge overview
  - `references` - Reference materials
  - `step{n}-{descriptor}` - Challenge step with number and descriptor

Examples:
- `ifs-ready-overview.md`
- `ifs-agent-step1-principles.md`
- `ifs-aihub-references.md`

## Content Structure Standards

### Main Challenge Pages

Each main challenge page (`ai-ready-challenge.md`, etc.) should include:

1. **Title and description**
2. **Challenge Steps** with links to individual steps
3. **Additional Resources** with links to overview and references
4. **Challenge Workflow** diagram using Mermaid
5. **Navigation** links to other challenges

### Step Pages

Each step page should include:

1. **Title** with step number and name
2. **Objectives** section outlining goals
3. **Activities** section with tasks
4. **Guidance/Content** section with relevant information
5. **Navigation** links to previous/next steps

### Overview Pages

Each challenge overview page should include:

1. **Introduction** with context
2. **Prerequisites** if applicable
3. **Challenge Objectives**
4. **Challenge Structure** listing steps
5. **Challenge Workflow** diagram using Mermaid
6. **Success Framework** with indicators and outcomes
7. **Navigation** links

## Mermaid Diagram Standards

Each challenge should include consistent workflow diagrams using Mermaid:

```mermaid
flowchart LR
    Start([Start]) --> Step1
    Step1[Step 1 Name] --> Step2
    Step2 --> Step3
    Step3 --> End([End])
    
    classDef step fill:#0072C6,stroke:#025,color:white,stroke-width:2px
    classDef endpoint fill:#5CB85C,stroke:#4CAE4C,color:white,stroke-width:2px
    
    class Step1,Step2,Step3 step
    class Start,End endpoint
```

## Navigation Standards

Each page should include three types of navigation elements:

1. **Breadcrumb Navigation** at the top of the page
2. **Previous/Next Navigation** at the top of the page
3. **"Back to Top" Links** after each major section
4. **Bottom Navigation** at the bottom of the page with Previous, Next, and Home links

### Breadcrumb Navigation
```markdown
[Home](../../index.md) > [Challenge Name](../../challenge-name.md) > [Current Page](./current-page.md)
```

### Top Previous/Next Navigation
```markdown
- [⬅️ Previous: Previous Page](./previous-page.md)
- [Next: Next Page ➡️](./next-page.md)
```

### Back to Top Links
After each major section:
```markdown
[🔝 Back to Top](#section-heading-id)
```

### Bottom Navigation for Step Pages
```markdown
## Navigation
- [⬅️ Previous: Previous Step](./previous-step-file.md)
- [Next: Next Step ➡️](./next-step-file.md)
- [🏠 Challenge Home](../../challenge-home.md)
```

### Main Challenge Pages Bottom Navigation
```markdown
## Navigation
- [⬅️ Back to Home](./index.md)
- [Customer Story](./ifs-customer-story.md)
- [AI Ready Challenge](./ai-ready-challenge.md)
- [AI Agent Challenge](./ai-agent-challenge.md)
- [AI Hub Challenge](./ai-hub-challenge.md)
```

## Frontmatter Standards

Each page should include proper frontmatter:

```yaml
---
layout: default
title: Page Title
parent: Parent Section Title
nav_order: X
---
```

Where:
- `title` - Clear, descriptive title of the page
- `parent` - The parent section (e.g., AI Ready Challenge)
- `nav_order` - The order of the page in navigation (0 for overview, 1-N for steps)

## Versioning Guidelines

### Version Numbers

All documentation follows [Semantic Versioning](https://semver.org/):

1. **MAJOR** version (x.0.0): Incompatible changes that significantly alter content or structure
2. **MINOR** version (1.x.0): New content or features in a backward-compatible manner
3. **PATCH** version (1.0.x): Backward-compatible bug fixes, typo corrections, minor improvements

### Changelog Management

1. **Main CHANGELOG.md**: Records major version changes across the entire documentation set
2. **Challenge-specific CHANGELOGs**: Detail changes specific to each challenge folder
3. **Format**: Follow the [Keep a Changelog](https://keepachangelog.com/) format with Added, Changed, and Fixed sections

### Update Process

When updating documentation:

1. Update the `version` and `last_updated` in the frontmatter
2. Record changes in the appropriate CHANGELOG file
3. If changes affect multiple sections, update the main CHANGELOG.md

## Formatting Guidelines

### Headings and Hierarchy

1. Use `#` for page title, already specified in frontmatter
2. Use `##` for major sections
3. Use `###` for subsections
4. Use `####` for sub-subsections
5. Don't skip heading levels

### Navigation Elements

1. **Breadcrumbs**: Add at the top of each file:
   ```markdown
   [Home](../../index.md) > [Parent Page](../parent.md) > [Current Page](./current.md)
   ```

2. **Progress Indicators**: Include at the top of challenge steps:
   ```markdown
   **📊 Progress:** Step X of Y
   **⏱️ Estimated Time:** Z hours
   ```

3. **Navigation Links**: Add at top and bottom of challenge steps:
   ```markdown
   - [⬅️ Previous: Step X](./previous-step.md) | [Next: Step X ➡️](./next-step.md)
   ```

4. **Back to Top Links**: Add after each major section in long documents:
   ```markdown
   [Back to Top](#top)
   ```

### Table of Contents

Include a table of contents in longer documents:

```markdown
## Table of Contents
{:.no_toc}

* TOC
{:toc}
```

### Code Blocks

Always specify the language for syntax highlighting:

````markdown
```yaml
key: value
```
````

### Callouts and Notes

Use consistent formatting for callouts:

```markdown
> **Note**: Important information to highlight.

> **Warning**: Critical warnings that require attention.

> **Tip**: Helpful suggestions to improve implementation.
```

## Example File Set

A complete challenge should have this file structure:

```
ai-{challenge}-challenge.md
{nn}-{challenge}/
  ├── ifs-{challenge}-overview.md
  ├── ifs-{challenge}-references.md
  ├── ifs-{challenge}-step1-{descriptor}.md
  ├── ifs-{challenge}-step2-{descriptor}.md
  ├── ifs-{challenge}-step3-{descriptor}.md
  └── ifs-{challenge}-step4-{descriptor}.md
```

## References Organization

### Reference File Structure

All reference materials should be organized in the `/references/` folder with:

1. **Main references index.md**: Overview of all reference materials
2. **Challenge-specific reference files**: Separate files for each challenge
3. **Cross-challenge references**: Materials relevant to multiple challenges

### Reference Linking

When linking to references:

1. Link from challenge files to specific reference sections using anchors
2. Use relative paths for all internal links
3. Include reference lists at the end of challenge steps where applicable

Example reference link format:
```markdown
[Azure Well-Architected Framework](../references/ai-ready-references.md#azure-well-architected-framework)
```

## Image and Media Guidelines

### Image Organization

1. Store all images in `/media/images/` folder
2. Use descriptive filenames for images
3. Group images by challenge or concept when possible

### Image Formatting

1. Use Markdown image syntax: `![Alt Text](../media/images/image-name.png)`
2. Include descriptive alt text for accessibility
3. For diagrams, include a text description below the image
4. For architectural diagrams, include links to reference documentation

## Accessibility Guidelines

1. Use proper heading hierarchy
2. Include alt text for all images
3. Use sufficient color contrast
4. Avoid conveying information solely through color
5. Use descriptive link text instead of "click here"
6. Provide text alternatives for diagrams and flowcharts
