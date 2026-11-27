<div align="center">

<img alt="FacePlugin" src="https://raw.githubusercontent.com/Faceplugin-ltd/faceplugin-assets/main/brand/logo.png" width="380"/>

# Face Recognition + Liveness Detection — Linux / Docker

### On-premise face matching and passive anti-spoofing for eKYC, banking and access control

**Fully offline REST APIs for face recognition (1:1 / 1:N) and face liveness detection (PAD). Run on your own servers with Docker — no cloud, no per-match fees, and no biometric data leaving your infrastructure.**

<a href="https://faceplugin.com/"><img src="https://img.shields.io/badge/Website-faceplugin.com-0A66C2?style=for-the-badge&logo=googlechrome&logoColor=white" alt="FacePlugin website"></a>
<a href="https://doc.faceplugin.com/"><img src="https://img.shields.io/badge/Docs-doc.faceplugin.com-0A66C2?style=for-the-badge&logo=readthedocs&logoColor=white" alt="FacePlugin documentation"></a>
<a href="https://hub.docker.com/u/faceplugin"><img src="https://img.shields.io/badge/Docker%20Hub-faceplugin-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="FacePlugin Docker Hub"></a>
<a href="https://huggingface.co/spaces/FacePlugin-Ltd/FaceRecognition-LivenessDetection-SDK"><img src="https://img.shields.io/badge/Try-Online%20Demo-FF6F00?style=for-the-badge&logo=huggingface&logoColor=white" alt="Try FacePlugin online demo"></a>
<a href="https://faceplugin.com/contact-us/"><img src="https://img.shields.io/badge/Request-License%20%26%20Demo-FF6F00?style=for-the-badge" alt="Request a license"></a>

`face recognition SDK` · `passive liveness` · `1:1 verification` · `1:N identification` · `on-premise REST API` · `Docker` · `eKYC`

</div>

---

## What this repository is

This repository is the **Linux / Docker product hub** for FacePlugin’s **face recognition + face liveness** stack.

The previous project dump in this repo is **retired**. Use the maintained products below — each ships a runnable demo, docs, and the current Docker image or native runtime.

| You need | Go here |
| -------- | ------- |
| **Face recognition** HTTP API (detect, quality, 1:1, **1:N gallery**) | [FaceRecognition-Docker](https://github.com/Faceplugin-ltd/FaceRecognition-Docker) · image `faceplugin/face-recognition` |
| **Face liveness** HTTP API (passive PAD) | [FaceLivenessDetection-Docker](https://github.com/Faceplugin-ltd/FaceLivenessDetection-Docker) · image `faceplugin/face-liveness` |
| **Windows** recognition API | [FaceRecognition-Windows](https://github.com/Faceplugin-ltd/FaceRecognition-Windows) |
| **Windows** liveness API | [FaceLivenessDetection-Windows](https://github.com/Faceplugin-ltd/FaceLivenessDetection-Windows) |
| **On-device** recognition + liveness | [Choose your mobile platform](#on-device-face-recognition--liveness) |
| **Try in the browser** | [Hugging Face Space](https://huggingface.co/spaces/FacePlugin-Ltd/FaceRecognition-LivenessDetection-SDK) |
| **All platforms (hub)** | [Face-Recognition-SDK](https://github.com/Faceplugin-ltd/Face-Recognition-SDK) · [Face-Liveness-Detection-SDK](https://github.com/Faceplugin-ltd/Face-Liveness-Detection-SDK) |

Full protocol and licensing: **[doc.faceplugin.com](https://doc.faceplugin.com/)**.

---

## Why two Docker products?

| Product | Answers | Typical API | Default port |
| ------- | ------- | ----------- | ------------ |
| **Face recognition** | Who is this? Are these the same person? Is the capture usable? | `/api/detect` · `/api/quality` · `/api/match` · `/api/identify` | **8092** |
| **Face liveness** | Is this a live person, or a photo / screen / mask? | `/api/liveness` | **8093** |

Run **both** containers when your flow needs matching **and** anti-spoofing (remote onboarding, selfie-to-ID, account recovery). Run **one** when you only need that capability.

> **Note:** Older docs and Docker tags that mentioned a single combined `face-recognition-liveness-sdk` image referred to a previous packaging. New integrations should use **`faceplugin/face-recognition`** and **`faceplugin/face-liveness`** from the repositories linked above.

---

## Quick start (server)

### Face recognition (1:1 + 1:N)

```bash
docker pull faceplugin/face-recognition:latest
# Full setup, activate, Postman: https://github.com/Faceplugin-ltd/FaceRecognition-Docker
```

### Face liveness (passive PAD)

```bash
docker pull faceplugin/face-liveness:latest
# Full setup, activate, Postman: https://github.com/Faceplugin-ltd/FaceLivenessDetection-Docker
```

### Try the APIs online (no install)

Open the static demo that calls FacePlugin’s hosted playground API:

**[Face Recognition & Liveness — Hugging Face Space](https://huggingface.co/spaces/FacePlugin-Ltd/FaceRecognition-LivenessDetection-SDK)**

---

## What you can build

| Capability | Detail |
| ---------- | ------ |
| **Face detection** | Bounding box, landmarks, head pose, attributes |
| **Face quality (ICAO-style)** | Capture checks before enrollment or matching |
| **1:1 verification** | Similarity score between two faces |
| **1:N identification** | Search a live face against **your** gallery on your server |
| **Face templates** | Extract templates; store them in your own database |
| **Passive 2D liveness** | Presentation-attack detection from a single RGB image |
| **Attacks covered** | Printed photos, screen / video replays, 3D masks (product-dependent) |

Everything runs **on-premise**. Licensing is offline. Matching and liveness checks have **no per-call cloud fee**.

---

## On-device face recognition + liveness

Same engine family as the servers, for Android and iOS (and cross-platform wrappers). Clone the platform repo, place the engine from its **Releases** page, run the demo.

| Platform | Repository |
| -------- | ---------- |
| **Android** | [FaceRecognition-LivenessDetection-Android](https://github.com/Faceplugin-ltd/FaceRecognition-LivenessDetection-Android) |
| **iOS** | [FaceRecognition-LivenessDetection-iOS](https://github.com/Faceplugin-ltd/FaceRecognition-LivenessDetection-iOS) |
| **Flutter** | [FaceRecognition-LivenessDetection-Flutter](https://github.com/Faceplugin-ltd/FaceRecognition-LivenessDetection-Flutter) |
| **React Native** | [FaceRecognition-LivenessDetection-ReactNative](https://github.com/Faceplugin-ltd/FaceRecognition-LivenessDetection-ReactNative) |
| **.NET MAUI** | [FaceRecognition-LivenessDetection-DotNet-MAUI](https://github.com/Faceplugin-ltd/FaceRecognition-LivenessDetection-DotNet-MAUI) |
| **Ionic Capacitor** | [FaceRecognition-LivenessDetection-Ionic-Capacitor](https://github.com/Faceplugin-ltd/FaceRecognition-LivenessDetection-Ionic-Capacitor) |
| **Ionic Cordova** | [FaceRecognition-LivenessDetection-Ionic-Cordova](https://github.com/Faceplugin-ltd/FaceRecognition-LivenessDetection-Ionic-Cordova) |
| **JavaScript / Web** | [FaceRecognition-LivenessDetection-Javascript](https://github.com/Faceplugin-ltd/FaceRecognition-LivenessDetection-Javascript) |

Liveness **without** recognition (PAD only): [Face-Liveness-Detection-SDK](https://github.com/Faceplugin-ltd/Face-Liveness-Detection-SDK).

---

## Complete eKYC stack

| Step | Product hub |
| ---- | ----------- |
| Read passport / ID / driving licence | [ID-Document-Recognition-SDK](https://github.com/Faceplugin-ltd/ID-Document-Recognition-SDK) |
| Confirm the document capture is genuine | [ID-Document-Liveness-Detection-Docker](https://github.com/Faceplugin-ltd/ID-Document-Liveness-Detection-Docker) |
| Confirm the selfie is a live person | [FaceLivenessDetection-Docker](https://github.com/Faceplugin-ltd/FaceLivenessDetection-Docker) / mobile liveness |
| Match selfie ↔ document portrait | [FaceRecognition-Docker](https://github.com/Faceplugin-ltd/FaceRecognition-Docker) / mobile recognition |

---

## Frequently asked questions

<details>
<summary><b>Is this still a full Docker project?</b></summary>

No. This GitHub repository is now a **hub README** so customers land on the right, maintained products. The runnable Linux / Docker code lives in [FaceRecognition-Docker](https://github.com/Faceplugin-ltd/FaceRecognition-Docker) and [FaceLivenessDetection-Docker](https://github.com/Faceplugin-ltd/FaceLivenessDetection-Docker).
</details>

<details>
<summary><b>Do I need both recognition and liveness?</b></summary>

For remote identity verification, yes in most cases: liveness stops presentation attacks; recognition matches the person to an ID photo or a gallery. For attendance or access control with trusted capture, recognition alone may be enough. For gatekeeping a camera feed without enrollment, liveness alone may be enough.
</details>

<details>
<summary><b>Is this a cloud face recognition API?</b></summary>

No. Inference and galleries run on **your** servers or devices. FacePlugin does not receive your images or templates in production deployments. The Hugging Face Space is an optional online demo only.
</details>

<details>
<summary><b>Does it work offline / air-gapped?</b></summary>

Yes. Licences activate offline against a machine code. Runtime needs no FacePlugin network call.
</details>

<details>
<summary><b>Where are face templates stored?</b></summary>

In **your** database. The SDK returns templates; it does not host a FacePlugin cloud gallery.
</details>

<details>
<summary><b>Has FacePlugin face recognition been evaluated independently?</b></summary>

FacePlugin has a report card in NIST’s Face Recognition Technology Evaluation (FRTE). See [NIST FRTE report cards](https://face.nist.gov/frte/reportcards/11/faceplugin_000.html) and ask us for the current evaluation summary.
</details>

<details>
<summary><b>How do I get a license?</b></summary>

Start the Docker or native server, copy the machine code from the logs or `/api/machinecode`, then [contact FacePlugin](https://faceplugin.com/contact-us/) with your platform and use case. We return a key for that machine code.
</details>

---

## Support

| | |
| --- | --- |
| 🌐 Website | [faceplugin.com](https://faceplugin.com) |
| 📘 Documentation | [doc.faceplugin.com](https://doc.faceplugin.com) |
| 🤗 Hugging Face | [FacePlugin-Ltd](https://huggingface.co/FacePlugin-Ltd) · [Online demo](https://huggingface.co/spaces/FacePlugin-Ltd/FaceRecognition-LivenessDetection-SDK) |
| 🐳 Docker Hub | [faceplugin](https://hub.docker.com/u/faceplugin) |
| ✉️ Email | [info@faceplugin.com](mailto:info@faceplugin.com) |
| 💬 Telegram | [@FacePluginSupport](https://t.me/FacePluginSupport) |
| 📱 WhatsApp | [+1 (469) 278-4822](https://wa.me/14692784822) |

<div align="center">
<sub><b>Keywords:</b> face recognition Docker · face recognition Linux · face recognition REST API · face liveness detection Docker · passive liveness · presentation attack detection · face anti-spoofing · 1:1 face verification · 1:N face identification · face matching SDK · face detection · ICAO face quality · on-premise biometrics · offline face recognition · eKYC · KYC · identity verification · FaceRecognition-LivenessDetection-Docker · FacePlugin</sub>
</div>
