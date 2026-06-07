# Progress

## Current Milestone

The first visual polish pass is published from the Papercraft Games repository.

## Completed

- Confirmed Godot 4.5 and Blender 4.5 toolchain.
- Audited the official FPE runtime and metadata keys.
- Pinned official FPE `v1.0.11`.
- Defined the 16-demo atomic curriculum.
- Established durable planning, validation, and handoff rules.
- Built the LaunchBox-style Godot gallery shell.
- Authored 16 atomic FPE demos plus one sub-scene in Blender and GLB.
- Added real conversation, inventory, audio, water, trigger, animation, camera,
  physics, holdable, group, UI, and scene metadata examples.
- Added deterministic Blender generation and pinned FPE `v1.0.11`.
- Added Godot static validation, direct FPE runtime loading for every demo, and
  a verified local web export.
- Added GitHub Actions deployment modeled on `resistdesign/entailed`.
- Published the public repository at <https://github.com/papercraftgames/fpe-rush>.
- Verified GitHub Actions run `27100959933` completed successfully.
- Enabled GitHub Pages from `gh-pages:/`, approved the custom-domain
  certificate, and enforced HTTPS at <https://rush.foldedpaperengine.com/>.
- Confirmed Blender, GLB, and WAV assets are ordinary Git blobs; Git LFS is not
  used.
- Added the official Folded Paper Engine website logo to the gallery.
- Reworked the gallery into a styled, dismissible sheet with a persistent reopen
  control so each loaded demo can use the full viewport.
- Added reproducible paper materials, bevels, scene dressing, calibrated GLB
  lighting, improved camera framing, and per-demo color to all generated scenes.
- Transferred the repository from `resistdesign` to the `papercraftgames`
  organization without losing Pages, the custom domain, HTTPS, issues, or
  Actions history.

## Session Handoff

- Date: June 7, 2026
- Branch: `main`
- Implementation commit: `e0a4a8d` (`Polish gallery UI and demo presentation`)
- Verified: `./scripts/build_demos.sh`, `./scripts/ci/check.sh`, native 1280x720
  viewport captures with the gallery open and closed, repository transfer, and
  retained GitHub Pages configuration. Deployment run `27103113677` succeeded
  from `papercraftgames/fpe-rush`.

## Next Action

Run a browser interaction pass across all 16 demos after deployment and open
focused issues for any remaining per-demo visual or input polish.

## Known Risks

- Browser interaction across all 16 demos remains the final production smoke
  test; the native visual capture covered the initial scene and gallery states.
