# Awesome Image Generation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com) [![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

A curated list of AI image generation APIs, SDKs, and production-ready tools.
Focused on services developers can integrate today.

> Last verified: March 2026

### Related Lists

- [Awesome Video Generation](../awesome-video-generation)
- [Awesome Audio Generation](../awesome-audio-generation)

---

## Contents

- [Text-to-Image APIs](#text-to-image-apis)
- [Open Source Models](#open-source-models)
- [Open Source Frameworks and UIs](#open-source-frameworks-and-uis)
- [Image Editing and Enhancement](#image-editing-and-enhancement)
- [SDKs and Developer Tooling](#sdks-and-developer-tooling)
- [Infrastructure and Deployment](#infrastructure-and-deployment)
- [Evaluation and Observability](#evaluation-and-observability)
- [Templates and Example Projects](#templates-and-example-projects)
- [Learning Resources](#learning-resources)

---

## Text-to-Image APIs

- **[OpenAI GPT Image](https://platform.openai.com/docs/guides/images)** – `gpt-image-1`, `gpt-image-1.5`, `gpt-image-1-mini`. Natively multimodal generation, editing, and inpainting. DALL-E 2/3 deprecated May 2026. [API Reference](https://platform.openai.com/docs/api-reference/images) | SDK: Python, Node
- **[Black Forest Labs (FLUX Pro)](https://bfl.ai)** – FLUX 1.1 Pro and FLUX.2 (32B params) via REST API. From the creators of FLUX and Stable Diffusion. [Docs](https://docs.bfl.ml/quick_start/introduction) | Also on Replicate, fal.ai, Together AI
- **[Stability AI](https://stability.ai)** – Stable Diffusion 3.5 and Stable Image via REST API. Text-to-image, image-to-image, upscaling, inpainting. [Docs](https://platform.stability.ai/docs/api-reference)
- **[Google Imagen (Vertex AI)](https://cloud.google.com/vertex-ai)** – Imagen 4 via Vertex AI. Text-to-image, editing, outpainting, inpainting, customization. [Docs](https://docs.cloud.google.com/vertex-ai/generative-ai/docs/image/overview) | [API Reference](https://docs.cloud.google.com/vertex-ai/generative-ai/docs/model-reference/imagen-api) | SDK: Python (google-cloud-aiplatform), Node
- **[Adobe Firefly API](https://developer.adobe.com/firefly-services/)** – Image generation, editing, Photoshop automation, and Lightroom operations. Part of Firefly Services platform. [Docs](https://developer.adobe.com/firefly-services/docs/firefly-api/) | SDK: JS/TS (official)
- **[Ideogram](https://ideogram.ai)** – Known for high-quality text rendering in images. Ideogram 3.0 supports generation, remix, edit, and character reference. OpenAI-compatible interface. [Docs](https://developer.ideogram.ai)
- **[Recraft AI](https://www.recraft.ai/api)** – Raster and vector image generation. V4 model (Feb 2026). Background removal, inpainting, outpainting, vectorization. OpenAI-compatible interface. [Docs](https://www.recraft.ai/docs/api-reference/getting-started) | [ComfyUI Plugin](https://github.com/recraft-ai/ComfyUI-RecraftAI)
- **[Midjourney](https://www.midjourney.com)** – Official API released late 2025. Enterprise/Pro plan holders only; no public self-service access. [Docs](https://docs.midjourney.com)
- **[Amazon Titan Image Generator](https://aws.amazon.com/bedrock/)** – Text-to-image via AWS Bedrock. Image conditioning, color palette guidance, background removal, and variations. [Docs](https://docs.aws.amazon.com/bedrock/latest/userguide/titan-image-models.html) | SDK: Python (boto3), Java, PHP
- **[Leonardo AI](https://leonardo.ai/api)** – Text-to-image, image-to-image, and image-to-video. Webhooks, LoRA models, and "Get API Code" export from web UI. [Docs](https://docs.leonardo.ai/docs/getting-started) | SDK: [TypeScript](https://github.com/Leonardo-Interactive/leonardo-ts-sdk), [Python](https://pypi.org/project/Leonardo-Ai-SDK/)
- **[fal.ai](https://fal.ai)** – Serverless inference hosting 1000+ image models. Fastest diffusion inference engine. Hosts FLUX, SD, and more. SOC 2 compliant. [Docs](https://docs.fal.ai/model-apis) | SDK: Python, JS
- **[PixelAPI](https://pixelapi.dev)** – Pay-per-use AI image API running SDXL, FLUX Schnell, and FLUX Dev on owned GPUs. Background removal, 4x upscaling, text-to-image, and image-to-image at $0.003-$0.005/image. [Docs](https://pixelapi.dev/docs) | SDK: `pip install pixelapi` / `npm install pixelapi`

## Open Source Models

### FLUX Family (Black Forest Labs)

- **[FLUX.1 [schnell]](https://huggingface.co/black-forest-labs/FLUX.1-schnell)** – 12B param rectified flow transformer. 1-4 step generation. Fully open for commercial use. Apache 2.0. [GitHub](https://github.com/black-forest-labs/flux)
- **[FLUX.1 [dev]](https://huggingface.co/black-forest-labs/FLUX.1-dev)** – 12B param guidance-distilled model. High quality, competitive with closed-source. Non-commercial license.
- **[FLUX.2 [dev]](https://huggingface.co/black-forest-labs/FLUX.2-dev)** – 32B param model with generation, editing, and multi-reference combining.

### Stable Diffusion Family (Stability AI)

- **[Stable Diffusion 1.5](https://huggingface.co/stable-diffusion-v1-5/stable-diffusion-v1-5)** – 860M UNet, runs on consumer GPUs. Foundation for massive community ecosystem of LoRAs, fine-tunes, and extensions.
- **[Stable Diffusion XL (SDXL)](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0)** – Native 1024x1024. Improved text-in-image and limb generation. Base + refiner pipeline.
- **[Stable Diffusion 3.5 Large](https://huggingface.co/stabilityai/stable-diffusion-3.5-large)** – MMDiT architecture with three text encoders (including T5-XXL). Highest-quality Stability open model. [Turbo](https://huggingface.co/stabilityai/stable-diffusion-3.5-large-turbo)
- **[SDXL-Turbo](https://huggingface.co/stabilityai/sdxl-turbo)** – Adversarial distillation of SDXL enabling single-step generation.

### Other Open Models

- **[PixArt-Alpha / PixArt-Sigma](https://github.com/PixArt-alpha/PixArt-alpha)** – DiT-based T2I at 10.8% of SD1.5 training cost. Near-commercial quality. [HuggingFace](https://huggingface.co/PixArt-alpha/PixArt-Sigma-XL-2-1024-MS)
- **[Kandinsky 3](https://github.com/ai-forever/Kandinsky-3)** – Open-source T2I from AI Forever. 2x larger U-Net and 10x larger text encoder vs v2.x. [HuggingFace](https://huggingface.co/kandinsky-community/kandinsky-3)
- **[DeepFloyd IF](https://github.com/deep-floyd/IF)** – Cascaded pixel-space diffusion (64px → 256px → 1024px). Strong text rendering. Zero-Shot FID 6.66 on COCO.
- **[Playground v2.5](https://huggingface.co/playgroundai/playground-v2.5-1024px-aesthetic)** – Aesthetic-focused model fine-tuned on SDXL architecture.
- **[LCM / LCM-LoRA](https://github.com/luosiallen/latent-consistency-model)** – Latent Consistency Models enabling 2-4 step generation. LCM-LoRA is a lightweight ~100MB adapter for any SDXL model. [Diffusers Docs](https://huggingface.co/docs/diffusers/using-diffusers/inference_with_lcm)

## Open Source Frameworks and UIs

- **[ComfyUI](https://github.com/Comfy-Org/ComfyUI)** – Node-based graph UI and backend for diffusion models. Highly customizable, API-accessible. Supports SD, SDXL, Flux, and modern models. GPL-3.0. [Docs](https://docs.comfy.org/)
- **[AUTOMATIC1111 WebUI](https://github.com/AUTOMATIC1111/stable-diffusion-webui)** – Most widely used Gradio-based SD web UI. 161k+ stars. Extensive extension ecosystem. AGPL-3.0. [Wiki](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki)
- **[Fooocus](https://github.com/lllyasviel/Fooocus)** – Midjourney-inspired SDXL UI. Prompt-only workflow, no manual parameter tweaking. GPL-3.0.
- **[InvokeAI](https://github.com/invoke-ai/InvokeAI)** – Creative engine for SD models targeting professionals. Industry-leading WebUI. Apache 2.0. [Website](https://invoke.ai)
- **[Forge](https://github.com/lllyasviel/stable-diffusion-webui-forge)** – Fork of AUTOMATIC1111 with improved GPU memory management and performance. Compatible with A1111 extensions. AGPL-3.0.

## Image Editing and Enhancement

- **[ControlNet](https://huggingface.co/docs/diffusers/main/api/pipelines/controlnet_flux)** – Precise structural control for diffusion models via edge maps, depth, pose, normals. Available for SD1.5, SDXL, and Flux. [A1111 Extension](https://github.com/Mikubill/sd-webui-controlnet)
- **[IP-Adapter](https://github.com/tencent-ailab/IP-Adapter)** – Lightweight adapter (~100MB) for image-based prompting. New cross-attention layers for image feature conditioning. [Diffusers Docs](https://huggingface.co/docs/diffusers/main/en/using-diffusers/ip_adapter)
- **[Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN)** – Image and video upscaler, up to 8x. Handles real-world blind super-resolution with noise/artifact removal. BSD 3-Clause. [Replicate](https://replicate.com/nightmareai/real-esrgan)
- **[GFPGAN](https://github.com/TencentARC/GFPGAN)** – Face restoration from Tencent ARC. Restores facial details from degraded images. Often paired with Real-ESRGAN.

## SDKs and Developer Tooling

- **[HuggingFace Diffusers](https://github.com/huggingface/diffusers)** – The canonical PyTorch library for diffusion models. SD 1.5, SDXL, SD3, Flux, ControlNet, IP-Adapter, and more. [Docs](https://huggingface.co/docs/diffusers) | `pip install diffusers`
- **[Replicate SDK](https://replicate.com)** – Python/JS client for 50,000+ hosted ML models. Pay-per-second, no GPU management. [Docs](https://replicate.com/docs) | `pip install replicate` / `npm install replicate`
- **[OpenAI SDK](https://platform.openai.com/docs/api-reference/images)** – Official SDK for GPT Image generation and editing. `client.images.generate()` and `client.images.edit()`. `pip install openai` / `npm install openai`
- **[fal.ai SDK](https://fal.ai)** – Python and JS SDKs for serverless inference. Also a Vercel AI SDK provider. [Docs](https://docs.fal.ai) | `pip install fal-client` / `npm install @fal-ai/client`
- **[Gradio](https://www.gradio.app)** – Python library for building interactive ML demos and web UIs. Foundation for AUTOMATIC1111, Fooocus, and HuggingFace Spaces. Includes `gradio-client` for programmatic access. [GitHub](https://github.com/gradio-app/gradio) | `pip install gradio`

## Infrastructure and Deployment

### GPU Cloud Providers

- **[RunPod](https://www.runpod.io)** – GPU pods and serverless endpoints. 48% of serverless cold starts under 200ms. [Docs](https://docs.runpod.io)
- **[Modal](https://modal.com)** – Serverless Python GPU cloud. Sub-second cold starts. [Docs](https://modal.com/docs) | `pip install modal`
- **[Lambda Labs](https://lambdalabs.com)** – On-demand A100 and H100 GPUs. Competitive pricing (~$1.10/hr A100 80GB). [Docs](https://docs.lambdalabs.com)
- **[Replicate](https://replicate.com)** – Serverless model hosting for open-source image models. [Docs](https://replicate.com/docs)
- **[fal.ai](https://fal.ai)** – Fastest diffusion inference engine. 1000+ hosted models. [Docs](https://docs.fal.ai)
- **[Together AI](https://www.together.ai)** – Inference API for 200+ open models. [Docs](https://www.together.ai/inference)

### Image Storage and Delivery

- **[Cloudinary](https://cloudinary.com)** – Enterprise image/video CDN with AI-powered transformations. [Docs](https://cloudinary.com/documentation) | SDK: Python, Node, Ruby, PHP, Java, .NET
- **[Imgix](https://imgix.com)** – Real-time image processing CDN. URL-parameter-based transforms. Connects to existing S3/GCS storage. [Docs](https://docs.imgix.com)
- **[Cloudflare Images](https://developers.cloudflare.com/images/)** – Image CDN on Cloudflare's global network. Pre-defined variants for transformations.
- **[Backblaze B2](https://www.backblaze.com/cloud-storage)** – S3-compatible object storage at ~$0.006/GB/month. Free egress via Cloudflare. [Docs](https://www.backblaze.com/docs/cloud-storage-s3-compatible-api)

## Evaluation and Observability

- **[pytorch-fid](https://github.com/mseitzer/pytorch-fid)** – PyTorch FID (Fréchet Inception Distance) implementation. Measures distribution similarity between real and generated images. `pip install pytorch-fid`
- **[torch-fidelity](https://github.com/toshas/torch-fidelity)** – High-fidelity ISC, FID, KID, and PRC metrics. Supports InceptionV3, CLIP, DINOv2, VGG16 feature extractors. [Docs](https://torch-fidelity.readthedocs.io/) | `pip install torch-fidelity`
- **[ImageReward](https://github.com/THUDM/ImageReward)** – First general-purpose human preference reward model for T2I (NeurIPS 2023). Trained on 137k expert comparison pairs. [Paper](https://arxiv.org/abs/2304.05977)
- **[IQA-PyTorch](https://github.com/chaofengc/IQA-PyTorch)** – Comprehensive image quality toolbox. PSNR, SSIM, LPIPS, FID, NIQE, MUSIQ, TOPIQ, NIMA, BRISQUE, and more.
- **[CLIP Score](https://github.com/Lightning-AI/torchmetrics)** – Measures semantic alignment between text prompts and generated images using CLIP embeddings. Available via `torchmetrics.multimodal.CLIPScore`.

## Templates and Example Projects

- **[OpenAI Cookbook (GPT Image)](https://cookbook.openai.com/examples/generate_images_with_gpt_image)** – Official notebooks for image generation and editing with gpt-image-1.
- **[HuggingFace Diffusers Examples](https://github.com/huggingface/diffusers/tree/main/examples)** – Official scripts for DreamBooth, LoRA fine-tuning, ControlNet training, and more.
- **[Replicate Text-to-Image Collection](https://replicate.com/collections/text-to-image)** – Curated runnable models with inline API code examples.
- **[B2 Image Generation Prompt Flow](https://github.com/backblaze-b2-samples/image-generation-prompt-flow)** – Image generation pipeline with prompt flow and Backblaze B2 cloud storage integration.
- **[B2 Background Removal with Transformers.js](https://github.com/backblaze-b2-samples/b2-transformerjs-background-removal)** – Browser-based background removal using Transformers.js with Backblaze B2 storage.
- **[HuggingFace Spaces](https://huggingface.co/spaces)** – Free hosting for Gradio and Streamlit ML demos. Thousands of image generation demos. [Docs](https://huggingface.co/docs/hub/spaces-sdks-gradio)

## Learning Resources

- [OpenAI Images API Guide](https://platform.openai.com/docs/guides/images)
- [HuggingFace Diffusers Documentation](https://huggingface.co/docs/diffusers)
- [ComfyUI Documentation](https://docs.comfy.org/)
- [Black Forest Labs API Docs](https://docs.bfl.ml/quick_start/introduction)
- [Google Imagen on Vertex AI Guide](https://docs.cloud.google.com/vertex-ai/generative-ai/docs/image/overview)
- [Adobe Firefly API Tutorial](https://developer.adobe.com/firefly-services/docs/firefly-api/)

---

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first. PRs for new tools, corrections, and updates are appreciated.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
