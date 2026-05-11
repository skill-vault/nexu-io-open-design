# Phase 1 Notes: Foundation PR

## Implementation

<!-- Files created/modified; implementation decisions; migration inventory/classification; retained/deferred rationale; problems encountered; deviations from design -->

- Tailwind no-Preflight setup must use the official layered CSS imports in `apps/web/src/index.css`:
  ```css
  @layer theme, utilities;
  @import "tailwindcss/theme.css" layer(theme);
  @import "tailwindcss/utilities.css" layer(utilities);
  ```
- Keep Preflight excluded in Phase 1 and retain the project-owned border reset from Tailwind's Preflight contract so `border border-*` token utilities render solid borders.

## Verification

<!-- Commands run and results; screenshot artifact links/paths; exact baseline/development startup parameters or full commands; baseline/development service URLs; baseline/development namespace names; agent comparison scenario coverage; theme/accent matrix covered; observed drift; approved deviations -->
