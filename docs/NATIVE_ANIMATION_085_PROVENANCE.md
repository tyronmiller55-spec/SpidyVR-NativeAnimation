# Native Animation cumulative 0.8.5 source provenance

## Current user-approved cumulative integration — Nov 8, 2026

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
