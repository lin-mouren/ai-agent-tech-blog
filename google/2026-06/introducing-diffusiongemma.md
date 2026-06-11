---
title: "Introducing DiffusionGemma"
vendor: google
source_url: https://blog.google/innovation-and-ai/technology/developers-tools/diffusion-gemma-faster-text-generation/
published_at: 2026-06-10T16:00:00.000Z
crawled_at: 2026-06-11T02:00:54.904Z
word_count: 1379
reading_time_minutes: 7
tags: [gemini, llama, multimodal, agents, infrastructure, evaluation, api, product, enterprise, open-source]
---

# DiffusionGemma: 4x faster text generation

Jun 10, 2026

·

5 min read

Share

[x.com](https://twitter.com/intent/tweet?text=DiffusionGemma%3A%204x%20faster%20text%20generation%20%40google&url=https://blog.google/innovation-and-ai/technology/developers-tools/diffusion-gemma-faster-text-generation/) [Facebook](https://www.facebook.com/sharer/sharer.php?caption=DiffusionGemma%3A%204x%20faster%20text%20generation&u=https://blog.google/innovation-and-ai/technology/developers-tools/diffusion-gemma-faster-text-generation/) [LinkedIn](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/innovation-and-ai/technology/developers-tools/diffusion-gemma-faster-text-generation/&title=DiffusionGemma%3A%204x%20faster%20text%20generation) [Mail](mailto:?subject=DiffusionGemma%3A%204x%20faster%20text%20generation&body=Check%20out%20this%20article%20on%20the%20Keyword:%0A%0ADiffusionGemma%3A%204x%20faster%20text%20generation%0A%0AAn%20overview%20of%20DiffusionGemma,%20an%20exceptionally%20fast%20text%20generation%20model%20with%20up%20to%204x%20faster%20speeds.%0A%0Ahttps://blog.google/innovation-and-ai/technology/developers-tools/diffusion-gemma-faster-text-generation/)

Copy link

Our newest open experimental model delivers up to 4x faster inference on dedicated GPUs and opens the door to exploring speed-critical, interactive local workflows.


B

Brendan O'Donoghue

Research Scientist


S

Sebastian Flennerhag

Research Scientist


Share

[x.com](https://twitter.com/intent/tweet?text=DiffusionGemma%3A%204x%20faster%20text%20generation%20%40google&url=https://blog.google/innovation-and-ai/technology/developers-tools/diffusion-gemma-faster-text-generation/) [Facebook](https://www.facebook.com/sharer/sharer.php?caption=DiffusionGemma%3A%204x%20faster%20text%20generation&u=https://blog.google/innovation-and-ai/technology/developers-tools/diffusion-gemma-faster-text-generation/) [LinkedIn](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/innovation-and-ai/technology/developers-tools/diffusion-gemma-faster-text-generation/&title=DiffusionGemma%3A%204x%20faster%20text%20generation) [Mail](mailto:?subject=DiffusionGemma%3A%204x%20faster%20text%20generation&body=Check%20out%20this%20article%20on%20the%20Keyword:%0A%0ADiffusionGemma%3A%204x%20faster%20text%20generation%0A%0AAn%20overview%20of%20DiffusionGemma,%20an%20exceptionally%20fast%20text%20generation%20model%20with%20up%20to%204x%20faster%20speeds.%0A%0Ahttps://blog.google/innovation-and-ai/technology/developers-tools/diffusion-gemma-faster-text-generation/)

Copy link



Today, we’re introducing DiffusionGemma, an experimental open model that explores text diffusion, an exceptionally fast approach to text generation. Released under an Apache 2.0 license, this 26B Mixture of Experts (MoE) model moves beyond the sequential token-by-token processing of typical autoregressive Large Language Models (LLMs). Instead, it generates entire blocks of text simultaneously, delivering up to 4x faster text generation on GPUs.



Built upon the industry-leading intelligence-per-parameter of our Gemma 4 family and cutting-edge [Gemini Diffusion research](https://deepmind.google/models/gemini-diffusion/), DiffusionGemma integrates a novel diffusion head designed to maximize generation speed. While autoregressive Gemma 4 models remain the standard for high-quality production outputs, DiffusionGemma is designed for researchers and developers exploring speed-critical, interactive local workflows such as in-line editing, rapid iteration, and generating non-linear text structures.

## Unlocking new value for developers

Developers building real-time interactive AI applications often struggle with the latency bottlenecks of local inference. DiffusionGemma addresses these challenges directly, with some key trade-offs:

- **Blazing fast inference:** By shifting the decode bottleneck from memory-bandwidth to compute, DiffusionGemma generates up to 4x faster token output on dedicated GPUs. (1000+ tokens per second on a single NVIDIA H100, 700+ tokens per second on NVIDIA GeForce RTX 5090).


[1](https://blog.google/innovation-and-ai/technology/developers-tools/diffusion-gemma-faster-text-generation/#footnote-1)
- **Accessible hardware footprint:** Operating as a 26B total Mixture of Experts (MoE) model that activates only 3.8B parameters during inference, DiffusionGemma fits comfortably within 18GB VRAM limits of high-end dedicated consumer GPUs when quantized.
- **Bi-directional attention**: Generating 256 tokens in parallel with each forward pass allows every token to attend to all others. This provides significant advantages for non-linear domains such as in-line editing, code infilling, amino acid sequences or mathematical graphs.
- **Intelligent self-correction:** The model iteratively refines its own output, allowing it to evaluate the entire text block at once to fix mistakes in real-time.
- **Experimental status & production recommendations:** Because it prioritizes speed and parallel layout generation, DiffusionGemma’s overall output quality is lower than standard Gemma 4. For applications that demand maximum quality, we recommend deploying standard Gemma 4.



You can improve DiffusionGemma's performance on specific tasks through fine-tuning. In the example below, [Unsloth](https://unsloth.ai/docs/models/diffusiongemma) fine-tuned DiffusionGemma to play Sudoku — a task autoregressive models struggle with because each token depends on future tokens. DiffusionGemma's bi-directional attention makes this much easier.



Fine-tuned DiffusionGemma solving Sudoku.

## **Why diffusion for text?**

While the AI research community has explored diffusion-based text generation for years, applying it to large models has remained a challenge. DiffusionGemma changes this by shifting how models use hardware.

### **The trade-off with traditional models**

Most language models act like a typewriter, generating one token at a time from left to right. In the cloud, this is efficient because servers can batch thousands of user requests together to share the hardware load. But when run locally for a single user, this word-by-word process leaves your dedicated GPU or TPU underutilized — it spends most of its time simply waiting for the next "keystroke."

DiffusionGemma reverses this inefficiency. Instead of predicting words sequentially, it drafts an entire 256-token paragraph simultaneously. By giving the computer's processor a larger chunk of work at once, DiffusionGemma utilizes your hardware to its full potential. It upgrades your model inference from a single, sequential typewriter to a massive printing press that stamps the entire block of text simultaneously.

Sorry, your browser doesn't support embedded videos, but don't worry, you can [download it](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/dgemma_faster.mp4) and watch it with your favorite video player!

DiffusionGemma text-to-3D SVG demo by Hugging Face. Step-by-step generation.

This means DiffusionGemma's speedup is designed for local and low-concurrency inference. In high-QPS cloud serving, autoregressive models can be deployed to saturate compute efficiently, so DiffusionGemma's parallel decoding offers diminishing returns and can result in higher serving costs. The throughput advantage is strongest at low-to-medium batch sizes on a single accelerator.

### **How text diffusion works**

Similar to AI image generators that [start with visual static and iteratively refine it](https://research.google/blog/on-device-diffusion-plugins-for-conditioned-text-to-image-generation/) into a clear picture, DiffusionGemma applies this to text:

1. **The canvas:** The model starts with a canvas of random placeholder tokens.
2. **Iterative refinement:** The model makes multiple passes, locking in correct tokens and using them as context clues to refine the rest.
3. **Final polish:** The text converges into high-quality output.

Sorry, your browser doesn't support embedded videos, but don't worry, you can [download it](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Diffusion_Process_3_1.mp4) and watch it with your favorite video player!

Because the model can process the whole paragraph while generating, it unlocks new patterns of model behavior, like perfectly closing complex markdown formatting or generating and rendering code in near real-time.

### **Get started today**

- **Download the weights:** Access the experimental model weights (released under a permissive Apache 2.0 license) right now on Hugging Face.
- **Integrate & learn:** Learn more in our [DiffusionGemma developer guide](https://developers.googleblog.com/en/diffusiongemma-the-developer-guide). Or deep dive into [A Visual Guide to DiffusionGemma](https://newsletter.maartengrootendorst.com/p/a-visual-guide-to-diffusiongemma) to understand the mechanics under the hood.
- **Use your favorite development tools:** Serve the model efficiently using [MLX](https://huggingface.co/collections/mlx-community/diffusiongemma), [vLLM](https://vllm-project.github.io/2026/06/10/diffusion-gemma) (with integration supported by [Red Hat](https://huggingface.co/collections/RedHatAI/diffusiongemma-26b-a4b-it)), and [Hugging Face Transformers](https://huggingface.co/google/diffusiongemma-26B-A4B-it). For rapid experimentation, we are releasing a fine-tuning tutorial using [Hackable Diffusion](https://github.com/google/hackable_diffusion), a modular JAX toolbox designed for composability. You can also explore fine-tuning with [Unsloth](https://unsloth.ai/docs/models/diffusiongemma) and NVIDIA [NeMo](https://github.com/NVIDIA-NeMo/Automodel/blob/main/docs/guides/dllm/diffusiongemma.md). Additionally, official support for llama.cpp is arriving soon.
- **Experience optimized performance:** We worked with [NVIDIA](https://blogs.nvidia.com/blog/rtx-ai-garage-local-gemma-diffusion) to optimize across their hardware stack, ensuring compatibility with consumer setups (quantized for GeForce RTX 5090 and 4090 GPUs) alongside high performance on enterprise systems (Hopper and Blackwell using advanced NVFP4 kernels), including NVIDIA DGX Spark and DGX Station for local deskside deployment, and RTX PRO for AI professionals. Native support for NVFP4 (4-bit floating-point) accelerates compute throughput, allowing the model to run at faster speeds with near-lossless accuracy.
- **Try your way:** Run on your desktop dedicated GPU or in the cloud through [Gemini Enterprise Agent Platform Model Garden](https://console.cloud.google.com/agent-platform/publishers/google/model-garden/diffusiongemma) or [NVIDIA NIM](https://catalog.ngc.nvidia.com/orgs/nim/teams/google/containers/diffusiongemma-26b-a4b-it?version=latest).

POSTED IN:

Read more

* * *

More Information

* * *

[1](https://blog.google/innovation-and-ai/technology/developers-tools/diffusion-gemma-faster-text-generation/#footnote-source-1 "Jump up")

_Note: Because this speedup relies on exploiting the high arithmetic intensity of accelerators, unified-memory architectures like those in Apple Silicon Macs — which are often memory-bandwidth-bound rather than compute-bound during inference — may not see the same acceleration over autoregressive models like Gemma 4._

Collapse

* * *

### Related stories

[\\
\\
Developer tools **See what 3 builders are making with Gemma 4**\\
\\
By\\
\\
\\
\\
Amy Eisinger\\
\\
\\
Jun 09, 2026](https://blog.google/innovation-and-ai/technology/developers-tools/gemma-4-builders/)

[\\
\\
Developer tools **Bringing the latest Gemini models to Apple developers**\\
\\
By\\
\\
\\
\\
Nicholas McNamara\\
\\
\\
\\
&\\
\\
\\
Thevi Sundaralingam\\
\\
\\
Jun 08, 2026](https://blog.google/innovation-and-ai/technology/developers-tools/bringing-gemini-models-to-apple-developers/)

[\\
\\
Developer tools **Gemma 4 QAT models: Optimizing model compression for mobile and laptop efficiency**\\
\\
By\\
\\
\\
\\
Olivier Lacombe\\
\\
\\
\\
&\\
\\
\\
Omar Sanseviero\\
\\
\\
Jun 05, 2026](https://blog.google/innovation-and-ai/technology/developers-tools/quantization-aware-training-gemma-4/)

[\\
\\
Developer tools **Kaggle is making AI benchmark creation effortless**\\
\\
By\\
\\
\\
\\
Nicholas Kang\\
\\
\\
\\
&\\
\\
\\
Andrew Wang\\
\\
\\
Jun 04, 2026](https://blog.google/innovation-and-ai/technology/developers-tools/build-kaggle--benchmarks-locally/)

[\\
\\
Developer tools **Introducing Gemma 4 12B: a unified, encoder-free multimodal model**\\
\\
By\\
\\
\\
\\
Olivier Lacombe\\
\\
\\
\\
&\\
\\
\\
Gus Martins\\
\\
\\
Jun 03, 2026](https://blog.google/innovation-and-ai/technology/developers-tools/introducing-gemma-4-12b/)

[\\
\\
AI **How we used Gemini to build Google I/O 2026**\\
\\
By\\
\\
\\
\\
Marvin Chow\\
\\
\\
Jun 01, 2026](https://blog.google/innovation-and-ai/technology/ai/io-2026-google-ai/)

.

Jump to position 1
Jump to position 2
Jump to position 3
Jump to position 4
Jump to position 5
Jump to position 6



Let’s stay in touch. Get the latest news from Google in your inbox.

[Subscribe](https://blog.google/newsletter-subscribe/) No thanks

Survey

Help us improve The Keyword with a one-question survey

YesNo

This survey is anonymous. All responses will be aggregated and used only for analysis to improve our services.

Did this article provide the level of detail you were looking for?

Yes, I got what I neededNo, I wanted more technical depthNo, I wanted a simpler overviewI was looking for something else entirely

✅

Thank you!