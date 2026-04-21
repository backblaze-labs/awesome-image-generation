# Awesome Image Generation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com) [![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

A curated list of AI image generation APIs, SDKs, and production-ready tools. Focused on services developers can integrate today.

Maintained by [Backblaze](https://www.backblaze.com).

### Related Lists

- [Awesome Audio Generation](https://github.com/backblaze-labs/awesome-audio-generation)
- [Awesome Video Generation](https://github.com/backblaze-labs/awesome-video-generation)
- [Awesome ML Data Pipelines](https://github.com/backblaze-labs/awesome-ml-data-pipelines)
- [Awesome Multimodal Data](https://github.com/backblaze-labs/awesome-multimodal-data)
- [Awesome Agent Infrastructure](https://github.com/backblaze-labs/awesome-agent-infrastructure)
- [Awesome Physical AI](https://github.com/backblaze-labs/awesome-physical-ai)

## Contents

- [Text-to-Image APIs](#text-to-image-apis)
- [Open Source Models](#open-source-models)
- [Open Source Frameworks and UIs](#open-source-frameworks-and-uis)
- [Image Editing and Enhancement](#image-editing-and-enhancement)
- [SDKs and Developer Tooling](#sdks-and-developer-tooling)
- [GPU Cloud Providers](#gpu-cloud-providers)
- [Image Storage and Delivery](#image-storage-and-delivery)
- [Evaluation and Observability](#evaluation-and-observability)
- [Templates and Example Projects](#templates-and-example-projects)

---

## Text-to-Image APIs

> Commercial image-generation APIs with hosted inference and developer SDKs.

- **[Adobe Firefly API](https://developer.adobe.com/firefly-services/)** – Image generation, editing, Photoshop automation, and Lightroom operations. Part of Firefly Services platform. [Docs](https://developer.adobe.com/firefly-services/docs/firefly-api/) | SDK: JS/TS (official)
- **[Amazon Titan Image Generator](https://aws.amazon.com/bedrock/)** – Text-to-image via AWS Bedrock. Image conditioning, color palette guidance, background removal, and variations. [Docs](https://docs.aws.amazon.com/bedrock/latest/userguide/titan-image-models.html) | SDK: Python (boto3), Java, PHP
- **[Black Forest Labs (FLUX Pro)](https://bfl.ai)** – FLUX 1.1 Pro and FLUX.2 (32B params) via REST API. From the creators of FLUX and Stable Diffusion. Also on Replicate, fal.ai, Together AI. [Docs](https://docs.bfl.ml/quick_start/introduction)
- **[fal.ai](https://fal.ai)** – Serverless inference hosting 1000+ image models. Fastest diffusion inference engine. Hosts FLUX, SD, and more. SOC 2 compliant. [Docs](https://docs.fal.ai/model-apis) | SDK: Python, JS
- **[Google Gemini Image API](https://ai.google.dev/gemini-api/docs/image-generation)** – Native image generation via Gemini models (gemini-2.5-flash-image, gemini-3.1-flash-image-preview). Text-to-image, editing, multi-turn. Python/JS/Go/Java SDKs. Free tier via AI Studio. [Docs](https://ai.google.dev/gemini-api/docs) | SDK: Python (google-genai), JS (google/generative-ai), Go, Java
- **[Google Imagen (Vertex AI)](https://cloud.google.com/vertex-ai)** – Imagen 4 via Vertex AI. Text-to-image, editing, outpainting, inpainting, customization. [Docs](https://docs.cloud.google.com/vertex-ai/generative-ai/docs/image/overview) | SDK: Python (google-cloud-aiplatform), Node
- **[Ideogram](https://ideogram.ai)** – Known for high-quality text rendering in images. Ideogram 3.0 supports generation, remix, edit, and character reference. OpenAI-compatible interface. [Docs](https://developer.ideogram.ai)
- **[Leonardo AI](https://leonardo.ai/api)** – Text-to-image, image-to-image, and image-to-video. Webhooks, LoRA models, and "Get API Code" export from web UI. [Docs](https://docs.leonardo.ai/docs/getting-started) | SDK: [TypeScript](https://github.com/Leonardo-Interactive/leonardo-ts-sdk), [Python](https://pypi.org/project/Leonardo-Ai-SDK/)
- **[Midjourney](https://www.midjourney.com)** – Official API released late 2025. Enterprise/Pro plan holders only; no public self-service access. [Docs](https://docs.midjourney.com)
- **[OpenAI GPT Image](https://platform.openai.com/docs/guides/images)** – gpt-image-1, gpt-image-1.5, gpt-image-1-mini. Natively multimodal generation, editing, and inpainting. DALL-E 2/3 deprecated May 2026. [Docs](https://platform.openai.com/docs/api-reference/images) | SDK: Python, Node
- **[Recraft AI](https://www.recraft.ai/api)** – Raster and vector image generation. V4 model (Feb 2026). Background removal, inpainting, outpainting, vectorization. OpenAI-compatible interface. [Docs](https://www.recraft.ai/docs/api-reference/getting-started)
- **[Runware](https://runware.ai)** – Image generation API serving 400k+ models via proprietary Sonic Inference Engine. Text-to-image, inpainting, outpainting, upscaling. Pay-per-image pricing with $2 free trial. [Docs](https://runware.ai/docs/en/image-inference/introduction) | SDK: [Python](https://pypi.org/project/runware/), [JS](https://github.com/Runware/sdk-js)
- **[Stability AI](https://stability.ai)** – Stable Diffusion 3.5 and Stable Image via REST API. Text-to-image, image-to-image, upscaling, inpainting. [Docs](https://platform.stability.ai/docs/api-reference)
- **[xAI Image Generation API](https://docs.x.ai/developers/model-capabilities/images/generation)** – grok-imagine-image model via REST API. Text-to-image and image editing. Batch up to 10 images, 1k/2k resolution. OpenAI-compatible interface. [Docs](https://docs.x.ai/developers/rest-api-reference/inference/images) | SDK: Python (xai-sdk), JS (openai-compatible)

## Open Source Models

> Open-weight image-generation models you can run locally or self-host.

- **[FLUX.1 [schnell]](https://huggingface.co/black-forest-labs/FLUX.1-schnell)** – 12B param rectified flow transformer. 1-4 step generation. Fully open for commercial use. [Docs](https://github.com/black-forest-labs/flux)
- **[FLUX.1 Kontext [dev]](https://huggingface.co/black-forest-labs/FLUX.1-Kontext-dev)** – 12B param instruction-based image editing model. Edit existing images via text prompts; character/style reference without finetuning. Non-commercial license. [Docs](https://github.com/black-forest-labs/flux)
- **[DeepFloyd IF](https://github.com/deep-floyd/IF)** – Cascaded pixel-space diffusion (64px → 256px → 1024px). Strong text rendering. Zero-Shot FID 6.66 on COCO.
- **[LCM / LCM-LoRA](https://github.com/luosiallen/latent-consistency-model)** – Latent Consistency Models enabling 2-4 step generation. LCM-LoRA is a lightweight ~100MB adapter for any SDXL model. [Docs](https://huggingface.co/docs/diffusers/using-diffusers/inference_with_lcm)
- **[PixArt-Alpha / PixArt-Sigma](https://github.com/PixArt-alpha/PixArt-alpha)** – DiT-based T2I at 10.8% of SD1.5 training cost. Near-commercial quality. [Docs](https://huggingface.co/PixArt-alpha/PixArt-Sigma-XL-2-1024-MS)
- **[Kandinsky 3](https://github.com/ai-forever/Kandinsky-3)** – Open-source T2I from AI Forever. 2x larger U-Net and 10x larger text encoder vs v2.x. [Docs](https://huggingface.co/kandinsky-community/kandinsky-3)
- **[Chroma](https://huggingface.co/lodestones/Chroma)** – 8.9B FLUX-based open T2I model. Supports text-to-image, image-to-image, and inpainting via diffusers ChromaPipeline. Apache-2.0, designed as a finetuning base. [Docs](https://huggingface.co/docs/diffusers/en/api/pipelines/chroma)
- **[FLUX.1 [dev]](https://huggingface.co/black-forest-labs/FLUX.1-dev)** – 12B param guidance-distilled model. High quality, competitive with closed-source. Non-commercial license.
- **[FLUX.2 [dev]](https://huggingface.co/black-forest-labs/FLUX.2-dev)** – 32B param model with generation, editing, and multi-reference combining.
- **[GLM-Image](https://github.com/zai-org/GLM-Image)** – 16B hybrid autoregressive + diffusion model from Zhipu AI. Excels at text rendering inside images. Supports T2I and I2I. Runs via GlmImagePipeline in diffusers. [Docs](https://huggingface.co/zai-org/GLM-Image)
- **[HiDream-I1](https://github.com/HiDream-ai/HiDream-I1)** – 17B sparse diffusion transformer for text-to-image. Three variants (Full, Dev, Fast). Top benchmark scores; diffusers-native via HiDreamImagePipeline. [Docs](https://huggingface.co/HiDream-ai/HiDream-I1-Full)
- **[HunyuanImage 3.0](https://github.com/Tencent-Hunyuan/HunyuanImage-3.0)** – 80B MoE T2I model from Tencent (13B params activated per token). Multimodal understanding and generation. Instruct-distilled variant released Jan 2026. Tencent Community License. [Docs](https://huggingface.co/tencent/HunyuanImage-3.0)
- **[Lumina-Image 2.0](https://github.com/Alpha-VLLM/Lumina-Image-2.0)** – 2.6B DiT text-to-image model using Gemma-2-2B text encoder. Diffusers-native via Lumina2Pipeline. Supports fine-tuning and controllable generation. Apache-2.0. [Docs](https://huggingface.co/Alpha-VLLM/Lumina-Image-2.0)
- **[OmniGen2](https://github.com/VectorSpaceLab/OmniGen2)** – Unified T2I + instruction-based image editing model. Dual-path architecture with separate autoregressive LLM and diffusion transformer decoders. pip-installable, Apache-2.0. [Docs](https://huggingface.co/OmniGen2/OmniGen2)
- **[Playground v2.5](https://huggingface.co/playgroundai/playground-v2.5-1024px-aesthetic)** – Aesthetic-focused model fine-tuned on SDXL architecture.
- **[Qwen-Image](https://github.com/QwenLM/Qwen-Image)** – Alibaba's open-weight T2I family. Qwen-Image-2512 (text-to-image) and Qwen-Image-Edit variants. Strong text rendering including Chinese. Diffusers-native, Apache 2.0. [Docs](https://huggingface.co/Qwen/Qwen-Image-2512)
- **[SDXL-Turbo](https://huggingface.co/stabilityai/sdxl-turbo)** – Adversarial distillation of SDXL enabling single-step generation.
- **[Stable Diffusion 1.5](https://huggingface.co/stable-diffusion-v1-5/stable-diffusion-v1-5)** – 860M UNet, runs on consumer GPUs. Foundation for massive community ecosystem of LoRAs, fine-tunes, and extensions.
- **[Stable Diffusion 3.5 Large](https://huggingface.co/stabilityai/stable-diffusion-3.5-large)** – MMDiT architecture with three text encoders (including T5-XXL). Highest-quality Stability open model. [Docs](https://huggingface.co/stabilityai/stable-diffusion-3.5-large-turbo)
- **[Stable Diffusion XL (SDXL)](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0)** – Native 1024x1024. Improved text-in-image and limb generation. Base + refiner pipeline.
- **[Z-Image](https://github.com/Tongyi-MAI/Z-Image)** – 6B param T2I model family from Alibaba Tongyi-MAI. Variants include Turbo (sub-second inference), Omni-Base (gen+edit), and Edit. Diffusers-native, Apache-2.0. [Docs](https://huggingface.co/Tongyi-MAI/Z-Image-Turbo)

## Open Source Frameworks and UIs

> Graphical and programmatic interfaces for running diffusion pipelines.

- **[AUTOMATIC1111 WebUI](https://github.com/AUTOMATIC1111/stable-diffusion-webui)** – Most widely used Gradio-based SD web UI. 161k+ stars. Extensive extension ecosystem. [Docs](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki)
- **[ComfyUI](https://github.com/Comfy-Org/ComfyUI)** – Node-based graph UI and backend for diffusion models. Highly customizable, API-accessible. Supports SD, SDXL, Flux, and modern models. [Docs](https://docs.comfy.org/)
- **[Fooocus](https://github.com/lllyasviel/Fooocus)** – Midjourney-inspired SDXL UI. Prompt-only workflow, no manual parameter tweaking.
- **[InvokeAI](https://github.com/invoke-ai/InvokeAI)** – Creative engine for SD models targeting professionals. Industry-leading WebUI. [Docs](https://invoke.ai)
- **[Forge](https://github.com/lllyasviel/stable-diffusion-webui-forge)** – Fork of AUTOMATIC1111 with improved GPU memory management and performance. Compatible with A1111 extensions.
- **[AI Toolkit (ostris)](https://github.com/ostris/ai-toolkit)** – All-in-one training suite for diffusion models. GUI and CLI. Trains FLUX.1/2, SDXL, SD 1.5, Qwen-Image, HiDream, and video models on consumer hardware.
- **[ComfyUI Deploy](https://github.com/BennyKok/comfyui-deploy)** – Open-source deployment platform for ComfyUI workflows. Exposes versioned REST APIs for production and staging. Supports serverless GPU backends and self-hosting on Vercel/Neon. [Docs](https://docs.comfydeploy.com/)
- **[ComfyUI-Manager](https://github.com/Comfy-Org/ComfyUI-Manager)** – Extension for ComfyUI that installs, updates, and manages 800+ custom nodes via a GUI or CLI. Auto-installed with ComfyUI Desktop. [Docs](https://registry.comfy.org)
- **[DiffSynth-Studio](https://github.com/modelscope/DiffSynth-Studio)** – Python diffusion engine by ModelScope. Inference and LoRA training for FLUX.1/2, Qwen-Image, Z-Image, and JoyAI-Image. Low-VRAM optimizations, ControlNet, IP-Adapter support.
- **[diffusion-pipe](https://github.com/tdrussell/diffusion-pipe)** – Pipeline-parallel training script for diffusion models across multiple GPUs. Supports FLUX.1/2, Chroma, SDXL, SD3, HiDream, Qwen-Image, Z-Image, and Hunyuan. LoRA, full fine-tuning, and multi-GPU via DeepSpeed.
- **[kohya_ss](https://github.com/bmaltais/kohya_ss)** – Gradio-based GUI for Kohya's SD training scripts. Supports LoRA, DreamBooth, and fine-tuning for SD 1.5, SDXL, SD3, and FLUX.1.
- **[OneTrainer](https://github.com/Nerogar/OneTrainer)** – GUI and CLI training suite for diffusion models. Supports FLUX.1/2, Chroma, SD 1.5/2/3/XL, SDXL, PixArt, HiDream, and Hunyuan Video.
- **[stable-diffusion.cpp](https://github.com/leejet/stable-diffusion.cpp)** – Diffusion model inference in pure C/C++ with no external dependencies. Runs SD 1.x/2.x/XL/3.5, FLUX.1/2, Chroma, Qwen-Image, and Z-Image. CPU/CUDA/Metal/Vulkan backends.

## Image Editing and Enhancement

> Conditioning, adaptation, restoration, and upscaling tools.

- **[GFPGAN](https://github.com/TencentARC/GFPGAN)** – Face restoration from Tencent ARC. Restores facial details from degraded images. Often paired with Real-ESRGAN.
- **[Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN)** – Image and video upscaler, up to 8x. Handles real-world blind super-resolution with noise/artifact removal. [Docs](https://replicate.com/nightmareai/real-esrgan)
- **[IP-Adapter](https://github.com/tencent-ailab/IP-Adapter)** – Lightweight adapter (~100MB) for image-based prompting. New cross-attention layers for image feature conditioning. [Docs](https://huggingface.co/docs/diffusers/main/en/using-diffusers/ip_adapter)
- **[ControlNet](https://huggingface.co/docs/diffusers/main/api/pipelines/controlnet_flux)** – Precise structural control for diffusion models via edge maps, depth, pose, normals. Available for SD1.5, SDXL, and Flux. [Docs](https://github.com/Mikubill/sd-webui-controlnet)
- **[Krita AI Diffusion](https://github.com/Acly/krita-ai-diffusion)** – Plugin integrating diffusion-based generation into Krita. Inpaint, outpaint, upscale, and ControlNet workflows without leaving the canvas. Uses ComfyUI as backend. Supports FLUX, SD 1.5/XL, Z-Image, and Illustrious. [Docs](https://docs.interstice.cloud/)
- **[Upscayl](https://github.com/upscayl/upscayl)** – Desktop GUI for AI image upscaling on Linux, macOS, and Windows. Uses Real-ESRGAN and other models; up to 16x upscale. Requires Vulkan GPU. [Docs](https://upscayl.org)

## SDKs and Developer Tooling

> Libraries and client SDKs for integrating image generation into apps.

- **[Gradio](https://www.gradio.app)** – Python library for building interactive ML demos and web UIs. Foundation for AUTOMATIC1111, Fooocus, and HuggingFace Spaces. Includes gradio-client for programmatic access. [Docs](https://github.com/gradio-app/gradio) | SDK: Python (pip install gradio)
- **[HuggingFace Diffusers](https://github.com/huggingface/diffusers)** – The canonical PyTorch library for diffusion models. SD 1.5, SDXL, SD3, Flux, ControlNet, IP-Adapter, and more. [Docs](https://huggingface.co/docs/diffusers) | SDK: Python (pip install diffusers)
- **[Replicate SDK](https://github.com/replicate/replicate-python)** – Python/JS client for 50,000+ hosted ML models. Pay-per-second, no GPU management. [Docs](https://replicate.com/docs) | SDK: Python (pip install replicate), Node (npm install replicate)
- **[fal.ai SDK](https://github.com/fal-ai/fal-js)** – Python and JS SDKs for serverless inference. Also a Vercel AI SDK provider. [Docs](https://docs.fal.ai) | SDK: Python (pip install fal-client), Node (npm install @fal-ai/client)
- **[OpenAI SDK](https://platform.openai.com/docs/api-reference/images)** – Official SDK for GPT Image generation and editing. client.images.generate() and client.images.edit(). SDK: Python (pip install openai), Node (npm install openai)

## GPU Cloud Providers

> Serverless and on-demand GPU platforms for running image models.

- **[fal.ai (GPU)](https://fal.ai/pricing)** – Fastest diffusion inference engine. 1000+ hosted models. [Docs](https://docs.fal.ai)
- **[Lambda Labs](https://lambdalabs.com)** – On-demand A100 and H100 GPUs. Competitive pricing (~$1.10/hr A100 80GB). [Docs](https://docs.lambdalabs.com)
- **[Modal](https://modal.com)** – Serverless Python GPU cloud. Sub-second cold starts. [Docs](https://modal.com/docs) | SDK: Python (pip install modal)
- **[Replicate](https://replicate.com)** – Serverless model hosting for open-source image models. [Docs](https://replicate.com/docs)
- **[RunPod](https://www.runpod.io)** – GPU pods and serverless endpoints. 48% of serverless cold starts under 200ms. [Docs](https://docs.runpod.io)
- **[Together AI](https://www.together.ai)** – Inference API for 200+ open models. [Docs](https://www.together.ai/inference)
- **[WaveSpeed AI](https://wavespeed.ai)** – Serverless inference platform with 700+ image and video models. Sub-second cold starts for FLUX and other diffusion models. OpenAI-compatible REST API. [Docs](https://wavespeed.ai/docs) | SDK: Python, JS

## Image Storage and Delivery

> Object stores and CDNs suited to generated-image workloads.

- **[Backblaze B2](https://www.backblaze.com/cloud-storage)** – S3-compatible object storage at low cost. Free egress via Cloudflare. [Docs](https://www.backblaze.com/docs/cloud-storage-s3-compatible-api) | [B2 integration](https://www.backblaze.com/docs/cloud-storage-s3-compatible-api)
- **[Cloudflare Images](https://developers.cloudflare.com/images/)** – Image CDN on Cloudflare's global network. Pre-defined variants for transformations.
- **[Cloudinary](https://cloudinary.com)** – Enterprise image/video CDN with AI-powered transformations. [Docs](https://cloudinary.com/documentation) | SDK: Python, Node, Ruby, PHP, Java, .NET
- **[Imgix](https://imgix.com)** – Real-time image processing CDN. URL-parameter-based transforms. Connects to existing S3/GCS storage. [Docs](https://docs.imgix.com)

## Evaluation and Observability

> Metrics, leaderboards, and quality tooling for generated images.

- **[pytorch-fid](https://github.com/mseitzer/pytorch-fid)** – PyTorch FID (Fréchet Inception Distance) implementation. Measures distribution similarity between real and generated images. SDK: Python (pip install pytorch-fid)
- **[IQA-PyTorch](https://github.com/chaofengc/IQA-PyTorch)** – Comprehensive image quality toolbox. PSNR, SSIM, LPIPS, FID, NIQE, MUSIQ, TOPIQ, NIMA, BRISQUE, and more.
- **[CLIP Score](https://github.com/Lightning-AI/torchmetrics)** – Measures semantic alignment between text prompts and generated images using CLIP embeddings. Available via torchmetrics.multimodal.CLIPScore.
- **[ImageReward](https://github.com/THUDM/ImageReward)** – First general-purpose human preference reward model for T2I (NeurIPS 2023). Trained on 137k expert comparison pairs. [Docs](https://arxiv.org/abs/2304.05977)
- **[torch-fidelity](https://github.com/toshas/torch-fidelity)** – High-fidelity ISC, FID, KID, and PRC metrics. Supports InceptionV3, CLIP, DINOv2, VGG16 feature extractors. [Docs](https://torch-fidelity.readthedocs.io/) | SDK: Python (pip install torch-fidelity)

## Templates and Example Projects

> Reference implementations, demos, and starter projects.

- **[B2 Background Removal with Transformers.js](https://github.com/backblaze-b2-samples/b2-transformerjs-background-removal)** – Browser-based background removal using Transformers.js with Backblaze B2 storage. [B2 integration](https://github.com/backblaze-b2-samples/b2-transformerjs-background-removal)
- **[B2 Image Generation Prompt Flow](https://github.com/backblaze-b2-samples/image-generation-prompt-flow)** – Image generation pipeline with prompt flow and Backblaze B2 cloud storage integration. [B2 integration](https://github.com/backblaze-b2-samples/image-generation-prompt-flow)
- **[HuggingFace Diffusers Examples](https://github.com/huggingface/diffusers/tree/main/examples)** – Official scripts for DreamBooth, LoRA fine-tuning, ControlNet training, and more.
- **[HuggingFace Spaces](https://huggingface.co/spaces)** – Free hosting for Gradio and Streamlit ML demos. Thousands of image generation demos. [Docs](https://huggingface.co/docs/hub/spaces-sdks-gradio)
- **[OpenAI Cookbook (GPT Image)](https://cookbook.openai.com/examples/generate_images_with_gpt_image)** – Official notebooks for image generation and editing with gpt-image-1.
- **[Replicate Text-to-Image Collection](https://replicate.com/collections/text-to-image)** – Curated runnable models with inline API code examples.

---

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md). One entry per PR — edit `entries.yaml` only and let the maintainers regenerate `README.md`.

## License

Released under [CC0 1.0 Universal](LICENSE). You may copy, modify, and redistribute without attribution.

## About Backblaze B2

[Backblaze B2 Cloud Storage](https://www.backblaze.com/cloud-storage) is S3-compatible object storage designed for AI and media workloads. This list is maintained as part of our work making B2 a convenient storage layer for AI workflows.
