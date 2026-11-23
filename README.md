# cellar-models

Files that the desktop app of [Cellar](https://cellar.fm) downloads the first time AutoMix is turned on.

Each file is a release asset named by its name and the first 16 digits of its SHA-256. Cellar uses a file only when its hash is the one pinned in the build that asks for it. An asset is never replaced: another file gets another name.

## Release `files-1`

| Asset | Bytes | SHA-256 |
|---|---|---|
| `beat_this_small-0e668e679603e912.onnx` | 9,961,005 | `0e668e679603e9122a87e92badbf4861b2f762d75841caed6a9564dd7519d198` |
| `lead_voice_small-b52ae279a819e8cc.onnx` | 183,540 | `b52ae279a819e8cc84581d77dea3a26f65796dc163ebd3f4c6fde78cbaa01cf6` |
| `htdemucs-26607631a2877bba.onnx` | 186,961,622 | `26607631a2877bbab7887d74f94db73a9c86819782a18fc8b9c1c8aa26a4d52e` |

## Where each file comes from, and its terms

- **`beat_this_small`** finds beats and downbeats. It is an ONNX export of the small checkpoint of [Beat This!](https://github.com/CPJKU/beat_this) by Francesco Foscarin, Jan Schlüter and Gerhard Widmer. Its README says: "The code and the published model weights are released under the MIT license. Note that some of the training files are fully copyrighted or under limited Creative Commons licenses, and it is up to the user to assess whether this may impact their use case." Its license is in [`licenses/beat_this-LICENSE`](licenses/beat_this-LICENSE).
- **`lead_voice_small`** says where a lead voice sings. It is Cellar's own model.
- **`htdemucs`** separates a song into vocals, drums, bass and the rest. It is an ONNX export of `htdemucs` from [Demucs](https://github.com/facebookresearch/demucs) by Alexandre Défossez and others. The code of Demucs is under the MIT license, in [`licenses/demucs-LICENSE`](licenses/demucs-LICENSE). On the weights its author wrote (issue 327, 2022-05-23): "The model weights are not covered by the MIT license, and are provided only for scientific purposes."

Cellar is free and not commercial.
