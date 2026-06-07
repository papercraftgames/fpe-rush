# Progress

## Current Milestone

The cross-demo player, interaction, containment, and visual polish pass is
implemented locally.

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
- Added an authored standard-mode FPE paper player to all 16 primary demos.
- Added raised collision rails around every demo floor and expanded the staged
  play area so players and rigid objects remain contained.
- Added in-world interaction pedestals for event-driven demos that previously
  depended on the gallery Activate button, including speakers, cameras,
  animations, groups, sub-scenes, and frame events.
- Reworked generated scenes with layered paper floors, folded corners, inset
  mats, paper scraps, varied materials, softer calibrated lighting, and a
  constructed papercraft player silhouette.
- Added a play-mode HUD with per-demo interaction guidance and fixed the gallery
  close button so it remains a compact circular control.
- Extended static and runtime validation to require a standard-mode player and
  four boundary rails in every primary demo.

## Session Handoff

- Date: June 7, 2026
- Branch: `codex/polish-playable-demos`
- Base commit: `826e3cb` (`UI Fixes`)
- Implementation commit: `e7deb45` (`Polish playable demo scenes`)
- Draft PR: <https://github.com/papercraftgames/fpe-rush/pull/1>
- Work committed: regenerated all Blender/GLB scenes with players, containment
  rails, interaction pedestals, and layered papercraft styling; updated
  gallery/play HUD copy and validation.
- Verified: `./scripts/build_demos.sh`; `./scripts/ci/check.sh` including Godot
  import/parsing, all 16 catalog entries, all GLBs, FPE runtime player loading,
  boundary checks, and web export; Godot movie-frame capture at 1280x720 after
  correcting GLTF light overexposure. The in-app browser surface was unavailable
  in this session, so visual QA used Godot's renderer directly.

## Next Action

Commit and push this coherent polish pass, then run a production browser
interaction pass across all 16 demos after deployment.

## Known Risks

- Browser interaction across all 16 demos remains the final production smoke
  test because the in-app browser connector was unavailable during this pass.
- Godot reports known renderer/resource cleanup warnings at process exit; the CI
  wrapper filters those existing warnings and all project validation checks pass.
