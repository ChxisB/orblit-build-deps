# orblit-build-deps

Prebuilt static libraries that the Orblit engine build downloads. The install scripts in
`dist/scripts` of [ChxisB/orblit](https://github.com/ChxisB/orblit) fetch them from the
releases of this repository.

| Release tag | Contents | Licence |
| --- | --- | --- |
| `angle-chromium-8118` | ANGLE static libraries for Windows, macOS and iOS | BSD-3-Clause |
| `nir-25.3.1-2` | Mesa NIR static libraries and headers for Direct3D 12 | MIT |
| `accesskit-0.23.1` | AccessKit C bindings | MIT or Apache-2.0, and the Chromium licence in the archive |
| `swappy-2025-01-31` | Android Frame Pacing library | Apache-2.0 |

## Archives

The ANGLE, AccessKit and Swappy archives are prebuilt files stored under shorter names. They
are unchanged. Each keeps the licence terms of the library it holds.

The Mesa NIR archives are built here by `.github/workflows/nir.yml`. The sources are in
`nir/`. Mesa is pinned as the submodule `nir/mesa`. `nir/LICENSE.md` is the licence of the
build scripts. Pushing a tag that starts with `nir-` builds all eight variants and publishes
them as a release.

`SHA256SUMS.txt` lists the hash of every uploaded asset. Check a download with
`sha256sum --check --ignore-missing SHA256SUMS.txt`.
