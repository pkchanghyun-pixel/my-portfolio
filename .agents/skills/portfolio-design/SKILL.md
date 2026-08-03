---
name: portfolio-design
description: Propose, preview, and implement approved visual design changes for this portfolio's HTML and CSS. Use for requests involving layout, color, spacing, typography, cards, responsive behavior, or other website presentation changes.
---

# Portfolio Design

Preserve the portfolio's content while making deliberate, approval-based visual changes.

## Workflow

1. Inspect `index.html` and `style.css` before proposing changes.
2. Separate content changes from design changes. Do not alter names, copy, links, images, or project order unless explicitly requested.
3. Offer two or three concrete design options when the user asks for proposals. Include layout behavior, responsive behavior, and tradeoffs.
4. When visual comparison is requested, provide consistent mockups whose content and palette remain fixed so only the proposed design dimension changes.
5. Wait for explicit approval before editing files.
6. Apply only the approved design scope. Preserve unrelated user changes.
7. Verify CSS syntax, responsive breakpoints, Git diff, and working-tree status.
8. Commit and push only when requested or already established as part of the approved workflow.

## Current Design System

- Theme: Ice Cyber Blue, bright and technical.
- Background: `#f3f8ff` with restrained blue-cyan ambient gradients.
- Surface: translucent white cards and profile panel.
- Main text: `#10213b`.
- Muted text: `#64748b`.
- Primary accent: `#0077ff`.
- Secondary accent and hover: `#00b8d9`.
- Border: `rgba(0, 119, 255, 0.18)`.
- Use subtle shadows and thin borders; avoid dark page backgrounds and excessive neon.

## Default Layout

Use the approved Project Gallery layout unless the user selects another option:

- Place the profile introduction in a centered panel above the projects.
- Give all project cards equal visual weight.
- Use three columns on wide screens, two on tablets, and one on phones.
- Keep card heights visually consistent and align action links near the bottom.
- Center an incomplete final row when practical.
- Preserve readable contrast and visible keyboard focus behavior.

## Change Boundaries

- Prefer CSS-only edits for visual requests when the existing markup supports them.
- Modify HTML only when the approved design cannot be implemented accessibly with CSS alone.
- Do not replace local images with remote URLs or overwrite personalized content.
- Do not mix a palette change into a layout-only request.
- Do not claim a mockup element will appear in production unless corresponding markup or CSS is implemented.
