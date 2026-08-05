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
8. After an approved change passes validation, commit the scoped files and push to `origin/main` unless the user explicitly asks not to publish.

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
- For a 1120px desktop container, target about `20px` card padding, `10px` to `12px` internal gaps, and a `170px` media area when matching the original portfolio presentation.
- Size cards from the tallest real content plus the aligned action link; do not add large empty areas merely to make cards feel prominent.
- Keep titles and descriptions content-height driven. Never fix text to a height that clips wrapping lines.
- Reserve the same media slot in every card. Use the real image or video where available and a quiet topic graphic where media is absent.
- Preserve every source image's intrinsic aspect ratio. Use `object-fit: cover` for the approved robot tile so it fills the shared media slot without stretching; cropping is allowed for this asset.
- For other images, use `contain` by default and switch to `cover` only after explicit approval.
- Keep the action link near the bottom, but reduce card height before increasing the blank gap above it.
- On desktop, use complete three-card rows and center only an incomplete final row.

## Card Title Alignment

- Split every card heading into a small `.day-label` and a separate `.project-title` on the next line.
- For numbered lessons, show Korean labels such as `1일차`; use concise category labels such as `VISION AI` when no day number exists.
- Give every desktop and tablet heading the same fixed block height so one-line and two-line titles place descriptions on the same baseline.
- Size the shared block for the longest two-line title. If a title needs more than two lines, increase every card's shared height rather than clipping it.
- Use the professional Editorial Course Index treatment: a full-width metadata row, small cobalt square, and thin Mist Blue divider.
- Keep the metadata label at `0.9rem` and the project name around `1.3rem` in Deep Navy at `800` weight.
- On card hover, change only the metadata square to Teal with a restrained scale effect.
- Avoid pills, title background boxes, side bars, gradients, and oversized decorative elements.
- Remove the fixed title height and flex basis in the single-column mobile layout because cross-card alignment is no longer needed.

## CSS Implementation Defaults

- Implement approved changes in existing HTML and CSS files before adding markup or assets.
- Use a `.profile::before` badge when the existing header contains only a heading and subtitle.
- Use `:not(:has(img)):not(:has(iframe))::before` for consistent media placeholders without adding HTML.
- Use a topic-specific placeholder such as `HTML · CSS · JS · API` until the user supplies the final image, then replace the placeholder without changing card order or copy.
- Set the approved robot image and embedded video to the shared `170px` media height; use `object-fit: cover` so the robot tile has no letterbox gap.
- Use `margin-top: auto` on card actions so links align without fixed text heights.
- Render unavailable destinations as a non-clickable `.card-link.is-disabled` element with `aria-disabled="true"`; never use a fake URL.

## Change Boundaries

- Prefer CSS-only edits for visual requests when the existing markup supports them.
- Modify HTML only when the approved design cannot be implemented accessibly with CSS alone.
- Do not replace local images with remote URLs or overwrite personalized content.
- Do not mix a palette change into a layout-only request.
- Do not claim a mockup element will appear in production unless corresponding markup or CSS is implemented.
