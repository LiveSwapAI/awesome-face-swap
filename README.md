# Awesome Face Swap

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![GitHub stars](https://img.shields.io/github/stars/LiveSwapAI/awesome-face-swap?style=social)](https://github.com/LiveSwapAI/awesome-face-swap/stargazers)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](#contributing)

A curated list of **open-source face swapping tools, real-time webcam applications, research models, detection and provenance resources, and supporting libraries** for images, videos, streaming, and video calls.

Entries are chosen for working code, clear documentation, research value, and transparent maintenance status. The list is **not ranked**, and inclusion is **not an endorsement**. Star and last-commit badges update automatically, but they are not proof of quality, security, or license fitness.

> **Important:** Public source code does not mean the model weights are free for commercial use. Check code, checkpoints, datasets, and dependency licenses separately.

## Responsible Use

Only swap faces of people who have given informed consent. Do not use these tools for impersonation, fraud, harassment, political deception, or non-consensual intimate imagery. These activities are illegal in many jurisdictions, and a growing number of laws require disclosure of synthetic media (for example, the transparency obligations in the EU AI Act). Check the rules that apply where you live and publish.

If you publish synthetic media, consider labeling it and attaching provenance metadata (see [Detection & Provenance](#detection--provenance)).

## Contents

- [How to Choose](#how-to-choose)
- [Face Swap Applications](#face-swap-applications)
- [Real-Time & Virtual Camera](#real-time--virtual-camera)
- [Stable Diffusion & ComfyUI](#stable-diffusion--comfyui)
- [Research Models](#research-models)
- [Identity-Preserving Generation](#identity-preserving-generation)
- [Detection & Provenance](#detection--provenance)
- [Supporting Libraries](#supporting-libraries)
- [More Resources](#more-resources)
- [Selection Criteria](#selection-criteria)
- [Contributing](#contributing)
- [Maintainer](#maintainer)

## How to Choose

| If you want... | Start with |
| --- | --- |
| Ready-to-use image and video swapping | FaceFusion |
| Real-time webcam or video calls | Deep-Live-Cam or VisoMaster, plus a virtual camera |
| Swapping inside Stable Diffusion / ComfyUI | ReActor |
| To train your own model | Faceswap (DeepFaceLab is archived and mostly of historical interest) |
| Research baselines | SimSwap, then the diffusion-based models |
| To study defenses | The Detection & Provenance section |

## Face Swap Applications

| Project | Stars | Last commit | Highlights | Notes |
| --- | --- | --- | --- | --- |
| [FaceFusion](https://github.com/facefusion/facefusion) | ![Stars](https://img.shields.io/github/stars/facefusion/facefusion?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/facefusion/facefusion?style=flat-square) | Face manipulation toolkit for images and video with GUI and CLI workflows. | Check individual model terms. |
| [Deep-Live-Cam](https://github.com/hacksider/Deep-Live-Cam) | ![Stars](https://img.shields.io/github/stars/hacksider/Deep-Live-Cam?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/hacksider/Deep-Live-Cam?style=flat-square) | One-image face swapping for webcam and recorded video. | Check pretrained model restrictions. |
| [VisoMaster](https://github.com/visomaster/VisoMaster) | ![Stars](https://img.shields.io/github/stars/visomaster/VisoMaster?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/visomaster/VisoMaster?style=flat-square) | GUI tool for face swapping and editing in video, with live preview. | Check model terms. |
| [Rope](https://github.com/Hillobar/Rope) | ![Stars](https://img.shields.io/github/stars/Hillobar/Rope?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/Hillobar/Rope?style=flat-square) | Desktop GUI built on the InsightFace swapping workflow. | Useful desktop interface. |
| [roop-unleashed](https://github.com/C0untFloyd/roop-unleashed) | ![Stars](https://img.shields.io/github/stars/C0untFloyd/roop-unleashed?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/C0untFloyd/roop-unleashed?style=flat-square) | GUI-focused enhanced roop workflow. | Check upstream status before installing. |
| [Faceswap](https://github.com/deepfakes/faceswap) | ![Stars](https://img.shields.io/github/stars/deepfakes/faceswap?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/deepfakes/faceswap?style=flat-square) | Deep-learning face swap software covering extraction, training, and conversion. | Advanced training workflow. |
| [inswapper](https://github.com/haofanwang/inswapper) | ![Stars](https://img.shields.io/github/stars/haofanwang/inswapper?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/haofanwang/inswapper?style=flat-square) | Minimal swapping and restoration example using InsightFace. | Check weight licensing. |
| [face2face](https://github.com/SocAIty/face2face) | ![Stars](https://img.shields.io/github/stars/SocAIty/face2face?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/SocAIty/face2face?style=flat-square) | Python library for swapping, restoration, embeddings, and API integration. | Developer-oriented. |
| [DeepFaceLab](https://github.com/iperov/DeepFaceLab) | ![Stars](https://img.shields.io/github/stars/iperov/DeepFaceLab?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/iperov/DeepFaceLab?style=flat-square) | Influential training and video production toolkit. | **Archived**; historical and reference value. |
| [roop](https://github.com/s0md3v/roop) | ![Stars](https://img.shields.io/github/stars/s0md3v/roop?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/s0md3v/roop?style=flat-square) | The simple one-image approach that inspired much of the ecosystem. | **Archived**; repository currently includes a Stable Diffusion extension. |

## Real-Time & Virtual Camera

A swap app produces frames; a virtual camera device is what lets Zoom, Teams, or OBS see them as a camera source. Webcam output and a virtual camera are not the same thing.

**Applications**

| Project | Stars | Last commit | Highlights | Notes |
| --- | --- | --- | --- | --- |
| [Deep-Live-Cam](https://github.com/hacksider/Deep-Live-Cam) | ![Stars](https://img.shields.io/github/stars/hacksider/Deep-Live-Cam?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/hacksider/Deep-Live-Cam?style=flat-square) | Real-time webcam preview and swapping from a single source photo. | Virtual camera needs separate setup. |
| [VisoMaster](https://github.com/visomaster/VisoMaster) | ![Stars](https://img.shields.io/github/stars/visomaster/VisoMaster?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/visomaster/VisoMaster?style=flat-square) | Live preview workflows with editing controls. | Evaluate hardware requirements. |
| [DeepFaceLive](https://github.com/iperov/DeepFaceLive) | ![Stars](https://img.shields.io/github/stars/iperov/DeepFaceLive?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/iperov/DeepFaceLive?style=flat-square) | Classic real-time streaming and video-call workflow with pretrained and custom models. | **Archived**; Windows-centric setup. |

**Virtual camera plumbing**

| Project | Stars | Last commit | Use case |
| --- | --- | --- | --- |
| [OBS Studio](https://github.com/obsproject/obs-studio) | ![Stars](https://img.shields.io/github/stars/obsproject/obs-studio?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/obsproject/obs-studio?style=flat-square) | Streaming software that includes an OBS Virtual Camera on supported platforms. |
| [pyvirtualcam](https://github.com/letmaik/pyvirtualcam) | ![Stars](https://img.shields.io/github/stars/letmaik/pyvirtualcam?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/letmaik/pyvirtualcam?style=flat-square) | Python library for sending frames to a virtual camera. |
| [v4l2loopback](https://github.com/umlaeute/v4l2loopback) | ![Stars](https://img.shields.io/github/stars/umlaeute/v4l2loopback?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/umlaeute/v4l2loopback?style=flat-square) | Linux kernel module that creates virtual video devices. |

## Stable Diffusion & ComfyUI

| Project | Stars | Last commit | Highlights | Notes |
| --- | --- | --- | --- | --- |
| [sd-webui-reactor](https://github.com/Gourieff/sd-webui-reactor) | ![Stars](https://img.shields.io/github/stars/Gourieff/sd-webui-reactor?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/Gourieff/sd-webui-reactor?style=flat-square) | ReActor extension for AUTOMATIC1111-style Stable Diffusion UIs. | Check model terms. |
| [ComfyUI-ReActor](https://github.com/Gourieff/ComfyUI-ReActor) | ![Stars](https://img.shields.io/github/stars/Gourieff/ComfyUI-ReActor?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/Gourieff/ComfyUI-ReActor?style=flat-square) | ReActor nodes for ComfyUI workflows. | Check model terms. |

## Research Models

These are research implementations. **Many are not real-time** or packaged as end-user apps. Check each checkpoint's license; several are restricted to non-commercial research.

| Project | Stars | Last commit | Focus | Notes |
| --- | --- | --- | --- | --- |
| [SimSwap](https://github.com/neuralchen/SimSwap) | ![Stars](https://img.shields.io/github/stars/neuralchen/SimSwap?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/neuralchen/SimSwap?style=flat-square) | Identity-transfer approach for images and videos. | Classic research baseline. |
| [Ghost (sber-swap)](https://github.com/ai-forever/ghost) | ![Stars](https://img.shields.io/github/stars/ai-forever/ghost?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/ai-forever/ghost?style=flat-square) | One-shot video face swapping with identity and attribute preservation. | Research code. |
| [FaceDancer](https://github.com/felixrosberg/FaceDancer) | ![Stars](https://img.shields.io/github/stars/felixrosberg/FaceDancer?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/felixrosberg/FaceDancer?style=flat-square) | Pose- and occlusion-aware high-fidelity swapping. | Research code. |
| [InfoSwap](https://github.com/GGGHSL/InfoSwap-master) | ![Stars](https://img.shields.io/github/stars/GGGHSL/InfoSwap-master?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/GGGHSL/InfoSwap-master?style=flat-square) | Information-bottleneck approach to disentangling identity. | Research code. |
| [E4S](https://github.com/e4s2023/E4S2023) | ![Stars](https://img.shields.io/github/stars/e4s2023/E4S2023?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/e4s2023/E4S2023?style=flat-square) | Fine-grained swapping via regional GAN inversion. | Research code. |
| [MobileFaceSwap](https://github.com/Seanseattle/MobileFaceSwap) | ![Stars](https://img.shields.io/github/stars/Seanseattle/MobileFaceSwap?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/Seanseattle/MobileFaceSwap?style=flat-square) | Lightweight model for mobile and low-resource devices. | Research code. |
| [BlendFace](https://github.com/mapooon/BlendFace) | ![Stars](https://img.shields.io/github/stars/mapooon/BlendFace?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/mapooon/BlendFace?style=flat-square) | Re-designed identity encoder for face swapping. | Research code. |
| [DiffSwap](https://github.com/wl-zhao/DiffSwap) | ![Stars](https://img.shields.io/github/stars/wl-zhao/DiffSwap?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/wl-zhao/DiffSwap?style=flat-square) | Diffusion-based high-fidelity face swapping. | Research code. |
| [VFace](https://github.com/Sanoojan/VFace) | ![Stars](https://img.shields.io/github/stars/Sanoojan/VFace?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/Sanoojan/VFace?style=flat-square) | **WACV 2026** training-free diffusion-based video swapping; also hosts REFace (**WACV 2025**). | Check checkpoint's non-commercial restrictions. |
| [DreamID-V](https://github.com/bytedance/DreamID-V) | ![Stars](https://img.shields.io/github/stars/bytedance/DreamID-V?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/bytedance/DreamID-V?style=flat-square) | **2026** diffusion-transformer video face swapping. | Code and model resources announced in 2026. |

## Identity-Preserving Generation

Related to face swapping, but these generate new images conditioned on a face identity rather than replacing a face in existing media.

| Project | Stars | Last commit | Focus |
| --- | --- | --- | --- |
| [InstantID](https://github.com/instantX-research/InstantID) | ![Stars](https://img.shields.io/github/stars/instantX-research/InstantID?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/instantX-research/InstantID?style=flat-square) | Zero-shot identity-preserving generation. |
| [PuLID](https://github.com/ToTheBeginning/PuLID) | ![Stars](https://img.shields.io/github/stars/ToTheBeginning/PuLID?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/ToTheBeginning/PuLID?style=flat-square) | Pure and lightning ID customization for text-to-image models. |
| [IP-Adapter](https://github.com/tencent-ailab/IP-Adapter) | ![Stars](https://img.shields.io/github/stars/tencent-ailab/IP-Adapter?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/tencent-ailab/IP-Adapter?style=flat-square) | Image-prompt adapter, including FaceID variants. |
| [Arc2Face](https://github.com/foivospar/Arc2Face) | ![Stars](https://img.shields.io/github/stars/foivospar/Arc2Face?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/foivospar/Arc2Face?style=flat-square) | Generates face images from ArcFace identity embeddings. |
| [Face-Adapter](https://github.com/FaceAdapter/Face-Adapter) | ![Stars](https://img.shields.io/github/stars/FaceAdapter/Face-Adapter?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/FaceAdapter/Face-Adapter?style=flat-square) | Adapter for face reenactment and swapping with pretrained diffusion models. |

## Detection & Provenance

Resources for detecting manipulated media, evaluating synthetic content, and attaching provenance information.

| Project | Stars | Last commit | Use case |
| --- | --- | --- | --- |
| [DeepfakeBench](https://github.com/SCLBD/DeepfakeBench) | ![Stars](https://img.shields.io/github/stars/SCLBD/DeepfakeBench?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/SCLBD/DeepfakeBench?style=flat-square) | Unified benchmark and codebase for deepfake detection. |
| [FaceForensics++](https://github.com/ondyari/FaceForensics) | ![Stars](https://img.shields.io/github/stars/ondyari/FaceForensics?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/ondyari/FaceForensics?style=flat-square) | Dataset and benchmark for forgery detection. |
| [Celeb-DF](https://github.com/yuezunli/celeb-deepfakeforensics) | ![Stars](https://img.shields.io/github/stars/yuezunli/celeb-deepfakeforensics?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/yuezunli/celeb-deepfakeforensics?style=flat-square) | Large-scale deepfake video dataset. |
| [c2pa-rs](https://github.com/contentauth/c2pa-rs) | ![Stars](https://img.shields.io/github/stars/contentauth/c2pa-rs?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/contentauth/c2pa-rs?style=flat-square) | Rust SDK for reading and writing C2PA Content Credentials (provenance). |
| [LPIPS](https://github.com/richzhang/PerceptualSimilarity) | ![Stars](https://img.shields.io/github/stars/richzhang/PerceptualSimilarity?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/richzhang/PerceptualSimilarity?style=flat-square) | Learned perceptual similarity metric for evaluating results. |

For identity similarity between source and result, ArcFace embeddings from [InsightFace](#supporting-libraries) are the standard measure.

## Supporting Libraries

These projects are **not face swappers**. They support detection, parsing, blending, restoration, and inference.

| Project | Stars | Last commit | Use case |
| --- | --- | --- | --- |
| [InsightFace](https://github.com/deepinsight/insightface) | ![Stars](https://img.shields.io/github/stars/deepinsight/insightface?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/deepinsight/insightface?style=flat-square) | Face recognition and analysis toolkit whose models underpin many swap pipelines. |
| [GFPGAN](https://github.com/TencentARC/GFPGAN) | ![Stars](https://img.shields.io/github/stars/TencentARC/GFPGAN?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/TencentARC/GFPGAN?style=flat-square) | Face restoration and enhancement. |
| [CodeFormer](https://github.com/sczhou/CodeFormer) | ![Stars](https://img.shields.io/github/stars/sczhou/CodeFormer?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/sczhou/CodeFormer?style=flat-square) | Blind face restoration. |
| [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) | ![Stars](https://img.shields.io/github/stars/xinntao/Real-ESRGAN?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/xinntao/Real-ESRGAN?style=flat-square) | Image and video super-resolution. |
| [facexlib](https://github.com/xinntao/facexlib) | ![Stars](https://img.shields.io/github/stars/xinntao/facexlib?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/xinntao/facexlib?style=flat-square) | Face detection, landmark estimation, and parsing utilities. |
| [BasicSR](https://github.com/XPixelGroup/BasicSR) | ![Stars](https://img.shields.io/github/stars/XPixelGroup/BasicSR?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/XPixelGroup/BasicSR?style=flat-square) | Image and video restoration research framework. |
| [face-parsing.PyTorch](https://github.com/zllrunning/face-parsing.PyTorch) | ![Stars](https://img.shields.io/github/stars/zllrunning/face-parsing.PyTorch?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/zllrunning/face-parsing.PyTorch?style=flat-square) | BiSeNet face parsing, commonly used for blending masks. |
| [MediaPipe](https://github.com/google-ai-edge/mediapipe) | ![Stars](https://img.shields.io/github/stars/google-ai-edge/mediapipe?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/google-ai-edge/mediapipe?style=flat-square) | Cross-platform face landmarks and on-device pipelines. |
| [ONNX Runtime](https://github.com/microsoft/onnxruntime) | ![Stars](https://img.shields.io/github/stars/microsoft/onnxruntime?style=flat-square) | ![Last commit](https://img.shields.io/github/last-commit/microsoft/onnxruntime?style=flat-square) | Cross-platform inference backend for many face-swap models. |

## More Resources

- [Awesome Deepfake Generation and Detection](https://github.com/flyingby/Awesome-Deepfake-Generation-and-Detection) - Academic overview and links to research code.
- [Deepfakes Survey 2026](https://github.com/VectorInstitute/deepfakes-survey-2026) - Recent research taxonomy and citations.
- [Face Swap GitHub topic](https://github.com/topics/face-swap) - Discover additional repositories.
- [Faceswap GitHub topic](https://github.com/topics/faceswap) - Browse the broader project ecosystem.

## Selection Criteria

A project is a good fit when it has:

1. **Publicly accessible code** or a clearly documented open implementation.
2. A meaningful connection to face swapping, real-time processing, detection or provenance, or a necessary supporting step.
3. Usable documentation, runnable examples, model information, or strong research impact.
4. Clear attribution to the original developers and transparent maintenance or archival status.

We do not list closed-source-only services, duplicate forks without substantial new functionality, spam repositories, or projects making misleading performance claims. Notes on archival status are checked when an entry is added or updated and can go stale; please open an issue if you spot an outdated note.

## Contributing

Contributions are welcome! Open a pull request or issue with:

- Project name and the **original** GitHub repository URL.
- A one-sentence description and its category.
- Whether source code and downloadable weights are available.
- Known OS and GPU requirements, maintenance status, and licensing limitations (code and weights).

## Maintainer

Maintained by **[LiveSwapAI](https://liveswapai.com/)**. The maintainer operates a commercial face transformation product. This list excludes closed-source services, and the product is not listed as an entry.
