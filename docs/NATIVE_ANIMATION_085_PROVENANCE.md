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
