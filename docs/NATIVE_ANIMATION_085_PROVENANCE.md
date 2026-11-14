# Native Animation cumulative 0.8.5 source provenance

## Current user-approved cumulative integration — Nov 13, 2026 (46195f7)

Authoritative working source:
`46195f712689a8811aa3695b261a1e01c29b6908`
https://github.com/tyronmiller55-spec/SpidyVR/commit/46195f712689a8811aa3695b261a1e01c29b6908

Branch `feat/c6a8279-ports`: the build the owner played on Nov 13, 2026, in a
session of about 20 minutes from 10:24 PM PST (stamp `46195f7`). The stack is
`0a593c0` plus HYBRID movement and v2, move haptics, a stable heading, passive
legs, quick sidestep, handstand H1, camera modes (ANIM HEAD RIDE, SHOULDER
LIMIT, SNAP REALIGN 360), and the ported Nov 13 playtest fixes (fresh-push flip
break, air-crouch hysteresis, air facing sync retired).

Publication starts from live NativeAnimation main
`d2e5ec72dfd28fd1ba65c4282ef66a115e047eaf` (after PR #4), preserving history.
The user approved merging the previous commits and updating the CURRENT latest
beta to the last version they played at 11:43 PM PST Nov 13, 2026 (`t56u`),
and confirmed the testers' release is the one labeled CURRENT (`t57u`). That
approval is not a request to post to Discord.

Exact tree parity policy (same as before, verify with Git blob IDs and modes):
- All tracked files other than the two below match the working source exactly.
- `README.md` is publication-specific documentation.
- This provenance document is additional publication-only documentation.
- `.github/workflows/release.yml` remains deliberately omitted. No workflow, rule
  change or automatic publication is added.
- The existing `test logs` directory is unchanged from main and from `46195f7`.

Windows build of `46195f7` (22/22 CTest, Python protocol tests passed):
https://github.com/tyronmiller55-spec/SpidyVR/actions/runs/43540575990
Release asset `Spidy-0.8.6-win64-c6a8279-ports-46195f7.zip` (unpacks to
`Spidy-0.8.6-player-torso-46195f7`), SHA256
`307cff6a7d02f570d515c39c7d48d920373312edb6dfefb691dcb0e0e253e47b`,
18,260,967 bytes.

Known limits going into this CURRENT (fixes in progress, not in this source):
web drops on game hitches, arms deforming in animations, handstands rarely
catching, and weak stabilization outside animation.

## Earlier integration — Nov 12, 2026 (0a593c0)

Authoritative working source:
`c342baa570c6c451594b8aa2da2e2b6befb545f1`
https://github.com/tyronmiller55-spec/SpidyVR/commit/c342baa570c6c451594b8aa2da2e2b6befb545f1

Branch `docs/publish-0a593c0`: the tested build `0a593c0a7e117b29be6f469bdc056963e5564ade`
(branch `feat/legs-yx-hold`) plus one documentation-only commit (docs/CHANGELOG.md,
CAMERA_AND_SHOOTERS.md, LEG_HOLD.md, OWNERSHIP.md, PLAYERS.md, POINT_JUMP.md). Every
non-documentation path is identical to `0a593c0`.

Publication starts from live NativeAnimation main
`67b231c7881bbbd24777f68652d985513606953f` (after PR #3 and the README Download commit), preserving history. The
user approved publishing the last tested build at 05:14 PST Nov 12, 2026 (`t72u`);
that build was played in the user's 37-minute session from 03:49 PST Nov 12.

Exact tree parity policy (same as before, verify with Git blob IDs and modes):
- All tracked files other than the two below match the working source exactly.
- `README.md` is publication-specific documentation.
- This provenance document is additional publication-only documentation.
- `.github/workflows/release.yml` remains deliberately omitted. No workflow, rule
  change or automatic publication is added.

Cumulative over the previous release build `d0584e7`: `07447b8` (camera motion
amounts, HEAD ANGLE, SHOOTERS: LOCKED TO ARM, findable camera/shooter/legs sections,
LEG CONTROL with REALISTIC FLIPS, same-frame flip break and grip cancel, jumps
animated to the landing), `c128662` POINT JUMP, `bec50c8` LEG TOGGLE (replaced),
`694861c` PUNCH VIEW EASE, `0a593c0` LEG HOLD on Y+X.

Windows build of `0a593c0` (11/11 CTest, Python protocol tests passed):
https://github.com/tyronmiller55-spec/SpidyVR/actions/runs/43193535133
Release asset `Spidy-0.8.6-legs-yx-0a593c0-win64.zip`, SHA256
`ddaa502d9b346a031d175d200dc12675076b9f80be34233364e887f25b1dfaa1`.

## Earlier integration — Nov 9, 2026 (fbd114e)

Authoritative working source:
`fbd114ec56f9d9fe4f42e89de8697e7f6c1fb211`
https://github.com/tyronmiller55-spec/SpidyVR/commit/fbd114ec56f9d9fe4f42e89de8697e7f6c1fb211

Branch: `fix/review-launch-run-softball` (includes `fd56775` cancel/position/sliders
and `40c0cb9` session summary on top of earlier `09526f1`).

Publication starts from live NativeAnimation main
`689b1625d91f11a62a95c0b9e9da51a4c54c2bdb`, preserving the owner's already-merged
PR2 and its ancestry. The user explicitly approved integration at 09:41 PST
Nov 9, 2026 (`t29u`). That approval is not headset acceptance or a request to
post to Discord. In-progress ownership-update work on a separate working-repo
branch is intentionally excluded.

Exact tree parity policy (verify with Git blob IDs):
- All runtime, test, build-tool, resource, licence and other tracked files match
  the authoritative working source byte-for-byte.
- `README.md` is publication-specific documentation.
- This provenance document is additional publication-only documentation.
- `.github/workflows/release.yml` remains deliberately omitted, as in the earlier
  public snapshot. No workflow, rule change or automatic publication is added.

New cumulative behavior relative to the prior 09526f1 publication (also listed in
the README):
- No-shot grip cancel stay until another native animation starts.
- Position lock at animation↔SpidyVR handoffs (actor feet authority + residual logs).
- Point-launch facing toward momentum (headset still reports incorrect; not claimed fixed).
- Run speed slider (SpidyVR ground run only) with hand-back blend to native sprint.
- Slow-mo length slider through 1:30 plus INFINITE.
- Wrist marker smoothing shared with shot aim.
- Soft lock for grip webs and matching trigger web-ball enemy picks.
- Shareable session `-summary.json` beside the full report.

Verified Windows build from the exact working source:
https://github.com/tyronmiller55-spec/SpidyVR/actions/runs/42578019609

- 6/6 CTest suites and 192 Python tests across the protocol modules passed.
- Packaged embedded-Python import smoke passed. Windows builds compile XR/engine
  callers, but tests do not run the live game or headset.
- Workflow inputs `publish=false`, empty `tag`; commit/tag, release and Discord
  steps were skipped. Existing artifact ID13656610376, 18,133,220 bytes.
- Exact downloaded original ZIP SHA256:
  `5d7ae797ccbfa373471a7dab1b6adb2358be005ea69e97431c13f081c4d2e342`.
- CRC/safe-path checks, 91 entries, 41 AMD64 PE32+ binaries, module versions 0.8.5.0,
  required rays export, matching Command v7 host/rays and compiled source
  `fbd114e` verified. Standard VC++ x64/OpenXR prerequisites remain unchanged.

Existing owner-delivered ZIP name:
`Spidy-0.8.5-review-fixes-fbd114e-win64.zip`.
No new gameplay build is needed for README/provenance/workflow-policy differences.
No binaries, personal settings/logs, local build output or secrets are committed.
No new release/tag or Discord message is part of this integration.

**Still experimental:** exact-new-build headset validation remains pending.
Point-launch facing is reported still incorrect. Ownership-update redesign
(animation owns ground/parkour/jumps/landings; SpidyVR owns air and wallrun) is
in progress separately and is not included. Preserve settings and extract the
whole ZIP into a new writable folder; never mix modules. Undecided procedural-leg
bindings/directions and genuine native strafe clips/control hooks remain separate
gates. No new mechanic is claimed for those items.

## Earlier cumulative integration 09526f1 — retained historical record — Nov 8, 2026

Authoritative working source:
`09526f19f00b54819641f0bde080894105b10e85`
https://github.com/tyronmiller55-spec/SpidyVR/commit/09526f19f00b54819641f0bde080894105b10e85

Publication starts from live NativeAnimation main
`6436391f763cdf8e6cc5c9e0b284a6dca3a83c66`, preserving the owner's already-merged
PR1 and its ancestry. The user explicitly approved integration at 17:32 PST.
That approval is not headset acceptance or a request to post to Discord.

Exact tree parity policy (verify with Git blob IDs):
- All runtime, test, build-tool, resource, licence and other tracked files match
  the authoritative working source byte-for-byte.
- `README.md` is publication-specific documentation.
- This provenance document is additional publication-only documentation.
- `.github/workflows/release.yml` remains deliberately omitted, as in the earlier
  public snapshot. No workflow, rule change or automatic publication is added.

The source includes the cumulative action-origin/contact-only punch/ground-owner
repairs, indicator/cancel slice, player upper-torso solve/camera-anchor/actual-hand
work and remaining feedback-consumer fixes. Detailed contracts and caveats are in
`NATIVE_ARM_FEEDBACK_PLAYTEST.md`, `PLAYER_UPPER_TORSO_CONTRACT.md`,
`PLAYER_UPPER_TORSO_PLAYTEST.md`, `FEEDBACK_CANCEL_PLAYTEST.md` and
`ACTION_FRAME_PLAYTEST.md` in this directory.

Verified Windows build from the exact working source:
https://github.com/tyronmiller55-spec/SpidyVR/actions/runs/42544305988

- 6/6 CTest suites and 187 Python tests across seven modules passed.
- Packaged embedded-Python import smoke passed; five selected portable suites
  also passed. Windows builds compile XR/engine callers, but tests do not run the
  live game or headset.
- Workflow inputs `publish=false`, empty `tag`; commit/tag, release and Discord
  steps were skipped. Existing artifact ID13642064266, 18,123,529 bytes.
- Exact downloaded original ZIP SHA256:
  `f560c7b42669da8281170132a3f384ea32c9f30e4bfd340e2bff4ceee35fd4bc`.
- CRC/safe-path checks, 90 entries, 41 AMD64 PE32+ binaries, module versions0.8.5.0,
  required rays export, matching Commandv7 host/rays and compiled source09526f19f0
  verified. All21 packaged Python tools matched the source after newline
  normalization. Standard VC++ x64/OpenXR prerequisites remain unchanged.

Existing owner-delivered ZIP name:
`Spidy-0.8.5-native-feedback-09526f1-win64.zip`.
Its unique internal root retains the historical prefix
`Spidy-0.8.5-player-torso-09526f1`. The filename is not an old binary relabel:
compiled source, build log and original artifact digest establish new code.
No new gameplay build is needed for README/provenance/workflow-policy differences.
No binaries, personal settings/logs, local build output or secrets are committed.
No new release/tag or Discord message is part of this integration.

**Still experimental:** exact-new-build headset alignment/performance, actual
physical damage, indicator readability, no-shot cancellation, supported-ground
release and air/wallrun transitions need runtime evidence. Latest uploaded logs
stamp older78eabb8, not this cumulative build. Preserve settings and extract the
whole ZIP into a new writable folder; never mix modules. Undecided procedural-leg
bindings/directions, genuine native strafe clips/control hooks and an older crash
dump/stack remain separate gates. No new mechanic is claimed for those items.

## Earlier compatibility snapshot — retained historical record

The following describes the preceding snapshot, not current source or current
integration status:

# Native Animation 0.8.5 compatibility source provenance

This review snapshot derives from working commit
`78eabb802448078f98061675c616bdaa8f51fa8a`:
https://github.com/tyronmiller55-spec/SpidyVR/tree/native-animation-085-compat

It merges upstream 0.8.5 `5374ee2c4ad8999a09470278fa6503a1280dd130`
with four-fix baseline `6b5dab8e8bd2ea5c7531003494e148a7c3cbf102`.
Computed merge base: `bdd4c9150f81148c1175387c3833bb299b254e97`.

Windows test-build evidence:
https://github.com/tyronmiller55-spec/SpidyVR/actions/runs/42491838485
Consult its actual conclusion and artifacts; this document does not assert success.

The public repo retains its source-snapshot model: workflows are omitted.
Apart from this document and omitted workflow, source matches the working commit.
Existing main branches are not overwritten; this is a review branch/PR.

Modified GPL-3.0 community Native Animation playtest, not an official upstream
release. Headset behavior requires user testing. Extract the entire package
outside the game install, retaining all subfolders, then run Spidy Launcher.exe.
