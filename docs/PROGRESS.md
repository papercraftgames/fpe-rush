# Progress

## Current Milestone

The first usability polish pass is implemented locally after the Papercraft
Games repository transfer.

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
- Added visible "Try this" guidance for all 16 demos, a control reference card,
  keyboard gallery toggling, and catalog validation for per-demo interaction
  prompts.
- Fixed the gallery panel for browser viewports by enabling expanded stretch,
  reducing the close control, making the detail column scroll vertically, and
  keeping activation controls visible above metadata.
- Added per-demo explanation copy that states what each entry demonstrates, how
  FPE uses exported Blender/GLB metadata to do it, and the exact repository path
  for the demo artifact.

## Session Handoff

- Date: June 7, 2026
- Branch: `main`
- Implementation commit: `e0a4a8d` (`Polish gallery UI and demo presentation`)
- Local uncommitted polish: demo guidance/control pass, per-demo FPE
  explanations and repository links, catalog validation in
  `scripts/validate_project.gd`, and responsive web layout fixes in
  `project.godot`.
- Verified: `./scripts/build_demos.sh`, `./scripts/ci/check.sh`, native 1280x720
  viewport captures with the gallery open and closed, repository transfer, and
  retained GitHub Pages configuration. Deployment run `27103113677` succeeded
  from `papercraftgames/fpe-rush`. Re-ran `./scripts/ci/check.sh` after the
  local guidance/control pass, after the responsive gallery layout fix, and
  after adding explanation/link validation. Served `build/web` locally and
  smoke-tested the exported browser UI with no console errors; the explanation
  panel, action controls, repo button, and metadata repo path are reachable in
  the scrollable detail column.

## Next Action

Run a browser interaction pass across all 16 demos after deployment and open
focused issues for any remaining per-demo visual or input polish.

## Known Risks

- Browser interaction across all 16 demos remains the final production smoke
  test; the exported browser smoke test covered the initial scene, gallery
  layout, explanation content, and first-demo repo link placement.
