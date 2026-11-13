# onnx-models

Open-source neural network models converted to ONNX / ORT for on-device inference, plus the ONNX Runtime and
sherpa-onnx libraries and the Python / FFmpeg runtimes for Android. The files are attached to the release
[`m1`](https://github.com/dfgnrxty/onnx-models/releases/tag/m1).

Every file keeps the license of its original project. Copyright belongs to the original authors;
the full license texts are in [`licenses/`](licenses). SHA-256 of every file: [`SHA256SUMS`](SHA256SUMS).

The `tools-*` archives are `libpython.zip.so` / `libffmpeg.zip.so` from youtubedl-android 0.18.1
(Maven Central `io.github.junkfood02.youtubedl-android:library` and `:ffmpeg`), built from Termux packages.
Corresponding source code: [yausername/youtubedl-android@0.18.1](https://github.com/yausername/youtubedl-android/tree/0.18.1),
[termux/termux-packages](https://github.com/termux/termux-packages) (build scripts and patches),
[python/cpython](https://github.com/python/cpython), [FFmpeg/FFmpeg](https://github.com/FFmpeg/FFmpeg).

| File | Model | Original project | License |
|---|---|---|---|
| `asr--decoder.onnx`, `asr--encoder.int8.onnx`, `asr--joiner.onnx`, `asr--silero_vad.onnx`, `asr--tokens.txt` | GigaAM (speech recognition, Russian) + Silero VAD | [salute-developers/GigaAM](https://github.com/salute-developers/GigaAM), [snakers4/silero-vad](https://github.com/snakers4/silero-vad) | MIT |
| `demucs--htdemucs_fp16weights.onnx` | HT-Demucs (music source separation) | [facebookresearch/demucs](https://github.com/facebookresearch/demucs) | MIT |
| `upscale--realesr-general-x4v3.onnx` | Real-ESRGAN general x4v3 | [xinntao/Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) | BSD-3-Clause |
| `up_plus--x4plus.onnx` | Real-ESRGAN x4plus | [xinntao/Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) | BSD-3-Clause |
| `up_anime--anime6b.ort` | Real-ESRGAN x4plus anime 6B | [xinntao/Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) | BSD-3-Clause |
| `faces--gfpgan.onnx`, `faces--yunet.onnx` | GFPGAN v1.4 (face restoration) + YuNet (face detection) | [TencentARC/GFPGAN](https://github.com/TencentARC/GFPGAN), [opencv/opencv_zoo](https://github.com/opencv/opencv_zoo) | Apache-2.0; MIT |
| `denoise--scunet.onnx` | SCUNet (denoising) | [cszn/SCUNet](https://github.com/cszn/SCUNet) | Apache-2.0 |
| `dejpeg--fbcnn.onnx` | FBCNN (JPEG artifact removal) | [jiaxi-jiang/FBCNN](https://github.com/jiaxi-jiang/FBCNN) | Apache-2.0 |
| `colorize--ddcolor.ort` | DDColor (colorization) | [piddnad/DDColor](https://github.com/piddnad/DDColor) | Apache-2.0 |
| `inpaint--lama.onnx` | LaMa (inpainting) | [advimman/lama](https://github.com/advimman/lama) | Apache-2.0 |
| `nobg--isnet-general-use.onnx` | IS-Net / DIS (background removal) | [xuebinqin/DIS](https://github.com/xuebinqin/DIS) | Apache-2.0 |
| `nobg_pro--inspyrenet.onnx` | InSPyReNet (background removal) | [plemeri/InSPyReNet](https://github.com/plemeri/InSPyReNet) | MIT |
| `sam--decoder.onnx`, `sam--encoder.onnx` | MobileSAM (segmentation) | [ChaoningZhang/MobileSAM](https://github.com/ChaoningZhang/MobileSAM) | Apache-2.0 |
| `ml-arm64-v8a--engine.zip` | ONNX Runtime + sherpa-onnx, Android arm64-v8a | [microsoft/onnxruntime](https://github.com/microsoft/onnxruntime), [k2-fsa/sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) | MIT; Apache-2.0 |
| `ml-armeabi-v7a--engine.zip` | ONNX Runtime + sherpa-onnx, Android armeabi-v7a | [microsoft/onnxruntime](https://github.com/microsoft/onnxruntime), [k2-fsa/sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) | MIT; Apache-2.0 |
| `ml-x86_64--engine.zip` | ONNX Runtime + sherpa-onnx, Android x86_64 | [microsoft/onnxruntime](https://github.com/microsoft/onnxruntime), [k2-fsa/sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) | MIT; Apache-2.0 |
| `stems_fast--accompaniment.fp16.onnx`, `stems_fast--vocals.fp16.onnx` | Spleeter 2stems (vocals / accompaniment), fp16 | [deezer/spleeter](https://github.com/deezer/spleeter), [k2-fsa/sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) | MIT; Apache-2.0 |
| `tools-arm64-v8a--libpython.zip.so`, `tools-arm64-v8a--libffmpeg.zip.so` | Python 3 and FFmpeg for Android arm64-v8a (youtubedl-android 0.18.1, built by Termux) | [yausername/youtubedl-android](https://github.com/yausername/youtubedl-android), [termux/termux-packages](https://github.com/termux/termux-packages), [python/cpython](https://github.com/python/cpython), [FFmpeg/FFmpeg](https://github.com/FFmpeg/FFmpeg) | GPL-3.0; Python: PSF-2.0; FFmpeg: GPL |
| `tools-armeabi-v7a--libpython.zip.so`, `tools-armeabi-v7a--libffmpeg.zip.so` | Python 3 and FFmpeg for Android armeabi-v7a (youtubedl-android 0.18.1, built by Termux) | [yausername/youtubedl-android](https://github.com/yausername/youtubedl-android), [termux/termux-packages](https://github.com/termux/termux-packages), [python/cpython](https://github.com/python/cpython), [FFmpeg/FFmpeg](https://github.com/FFmpeg/FFmpeg) | GPL-3.0; Python: PSF-2.0; FFmpeg: GPL |
| `tools-x86_64--libpython.zip.so`, `tools-x86_64--libffmpeg.zip.so` | Python 3 and FFmpeg for Android x86_64 (youtubedl-android 0.18.1, built by Termux) | [yausername/youtubedl-android](https://github.com/yausername/youtubedl-android), [termux/termux-packages](https://github.com/termux/termux-packages), [python/cpython](https://github.com/python/cpython), [FFmpeg/FFmpeg](https://github.com/FFmpeg/FFmpeg) | GPL-3.0; Python: PSF-2.0; FFmpeg: GPL |
