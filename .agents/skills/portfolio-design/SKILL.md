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

- Theme: Education Tech Portfolio, bright and professional.
- Page background: Cloud `#f5f7fb`.
- Surface: White `#ffffff` for cards and the profile panel.
- Main text: Deep Navy `#17324d`.
- Muted text: Slate `#64748b`.
- Primary accent: Cobalt Blue `#315efb`.
- Secondary accent: Teal `#0ea5a4`.
- Media background: Soft Sky `#eef3f9`.
- Border: Mist Blue `#d8e2f0`.
- Use subtle shadows and thin borders; avoid dark page backgrounds, decorative gradients, and excessive neon.

## Headline Treatment

- Make the centered profile panel the visual entry point without changing its content.
- Add a compact uppercase portfolio badge above the name when the headline needs more identity.
- Use a strong Korean headline at roughly `2.5rem` to `2.75rem`, tight tracking, and a restrained line height.
- Keep the course subtitle smaller and blue so it supports rather than competes with the headline.
- Decorative rules may flank the title, but keep them short, solid cobalt, and visually secondary.
- Use a solid white profile panel on the Cloud page background. Do not add a headline gradient unless the user explicitly approves it.

## Default Layout

Use the approved Project Gallery layout unless the user selects another option:

- Place the profile introduction in a centered panel above the projects.
- Give all project cards equal visual weight.
- Use three columns on wide screens, two on tablets, and one on phones.
- Keep card heights visually consistent and align action links near the bottom.
- Center an incomplete final row when practical.
- Preserve readable contrast and visible keyboard focus behavior.

## Compact Project Cards

- Minimize unused vertical space while keeping every card in a row the same height.
- For a 1120px desktop container, target about `20px` card padding, `10px` to `12px` internal gaps, and a `120px` to `140px` media area.
- Size cards from the tallest real content plus the aligned action link; do not add large empty areas merely to make cards feel prominent.
- Keep titles and descriptions content-height driven. Never fix text to a height that clips wrapping lines.
- Reserve the same media slot in every card. Use the real image or video where available and a quiet topic graphic where media is absent.
- Preserve every source image's intrinsic aspect ratio. Prefer `object-fit: contain` or Figma `scaleMode: FIT`; use cropping only after explicit approval.
- When an image does not match the shared media slot, letterbox it with a quiet neutral background rather than stretching it.
- Keep the action link near the bottom, but reduce card height before increasing the blank gap above it.
- On desktop, preserve the balanced `3 + 2` arrangement with the final two cards centered.

## CSS Implementation Defaults

- Implement approved changes in existing HTML and CSS files before adding markup or assets.
- Use a `.profile::before` badge when the existing header contains only a heading and subtitle.
- Use `:not(:has(img)):not(:has(iframe))::before` for consistent media placeholders without adding HTML.
- Set real images to `object-fit: contain`; keep embedded video frames at the shared media height.
- Use `margin-top: auto` on card actions so links align without fixed text heights.

## Change Boundaries

- Prefer CSS-only edits for visual requests when the existing markup supports them.
- Modify HTML only when the approved design cannot be implemented accessibly with CSS alone.
- Do not replace local images with remote URLs or overwrite personalized content.
- Do not mix a palette change into a layout-only request.
- Do not claim a mockup element will appear in production unless corresponding markup or CSS is implemented.
