# Rented compute and open-source models for cheap 3D-style social video (state as of 17 November 2026)

Research conditions the report writer must know before using these notes:

- Direct page fetches were blocked by this session's network policy (huggingface.co, ltx.io, morphic.com and venturebeat.com all failed; the environment allows no web hosts), and the shared web-search budget ran out after 29 searches. Vendor pricing pages were therefore NOT opened directly.
- Three evidence grades are used below. **[P]** = primary source read directly in full (official GitHub repositories and docs cloned on 17 Nov 2026; commit date given). **[S]** = search-engine summary of a vendor or third-party page that I could not open (date given where the summary stated one). **[U]** = unverified recollection from model training data (mid-2026 or older), listed only under Gaps.
- No searches at all could be run for render farms, cloud PCs (Shadow, Vagon, AirGPU), late-2026 hardware prices, or user reports on learning curve. Those sections are mostly gaps and need a follow-up research pass.

## 1. Open-weights video models in November 2026: which exist, how close to closed models, VRAM, and speed

### Takeaway
The open-weights field in November 2026 is Wan 2.2 (still Alibaba's newest downloadable Wan; 2.5, 2.6, 2.7 and 3.0 are hosted-only), HunyuanVideo 1.5, LTX-2.5 (Aug 2026), MiniMax H3 (Aug 2026, currently the top-ranked open-weights model and near the closed top tier) and Kandinsky 6.0 (Oct 2026). All of them realistically need a 24–32 GB NVIDIA card plus 32–75 GB of system RAM, take roughly 25 seconds to 10+ minutes per 5-second 720p clip depending on distillation and quantisation, and two of them (HunyuanVideo 1.5, MiniMax H3) carry licences that exclude the EU and UK.

### Cited Findings

**Which versions are open**
- The official Wan2.2 repository lists five open models (T2V-A14B, I2V-A14B, TI2V-5B, S2V-14B, Animate-14B); its newest "Latest News" entry is 13 Nov 2025 and it mentions no Wan 2.5/2.6/2.7/3.0 weights. The repository licence is Apache 2.0. [P, repo last commit 21 Sep 2026] — [Wan-Video/Wan2.2 README](https://github.com/Wan-Video/Wan2.2/blob/main/README.md)
- ComfyUI's official docs list Wan 2.5, 2.6, 2.7 and 3.0 only as paid partner (API) nodes billed per second, while Wan 2.2 is the newest Wan with a local-weights tutorial. [P, 16 Nov 2026] — [Comfy docs: partner node pricing](https://github.com/Comfy-Org/docs/blob/main/tutorials/partner-nodes/pricing.mdx); [Comfy docs: Wan2.2 tutorial](https://github.com/Comfy-Org/docs/blob/main/tutorials/video/wan/wan2_2.mdx)
- Third-party checks dated 2 and 5 Nov 2026 found no Wan 2.7 or Wan 3.0 weights on Alibaba's official Hugging Face or GitHub organisations; Wan 3.0 launched as an API-only public beta on 6 Aug 2026. Some SEO pages claim Wan 2.7 is Apache-2.0 open; the sources that checked the repositories contradict them. [S] — [howaiworks.ai](https://howaiworks.ai/blog/alibaba-wan-open-weights-stopped-at-2-2); [kenerateai.com, Nov 2026](https://kenerateai.com/blogs/is-wan-3-0-open-source); [morphic.com](https://morphic.com/resources/models/wan-3-0); contradicted by [miraflow.ai](https://miraflow.ai/blog/wan-2.7-explained-open-and-advanced-large-scale-video-generative-models)
- Alibaba reportedly targeted November 2026 for a next-generation video model; as of 9 Nov it had no name, no release and no word on open weights. [S] — [eachlabs.ai](https://www.eachlabs.ai/blog/alibaba-next-gen-video-model-november)
- HunyuanVideo 1.5 (8.3B parameters, released 20–21 Nov 2025) is still Tencent's current open video release; the official repo's last news item is 23 Dec 2025 and no 2.0 is mentioned. [P, repo last commit 10 Apr 2026 — older than mid-2026] — [HunyuanVideo-1.5 README](https://github.com/Tencent-Hunyuan/HunyuanVideo-1.5/blob/main/README.md)
- LTX-2.5 (22B-parameter transformer, open weights, native multishot, synced audio, up to 4K HDR) was released 11 Aug 2026 and is the model Lightricks' own repo now recommends; LTX-2.3 preceded it in March 2026. [P, repo 12 Nov 2026; S for release date] — [Lightricks/LTX-2 README](https://github.com/Lightricks/LTX-2/blob/main/README.md); [Comfy docs: LTX-2.5](https://github.com/Comfy-Org/docs/blob/main/tutorials/video/ltx/ltx-2-5.mdx); [comfyui-wiki, 11 Aug 2026](https://comfyui-wiki.com/en/news/2026-08-11-ltx-2-5-open-weights-release)
- MiniMax H3 open weights landed 3 Aug 2026 with native ComfyUI support. Officially it is a 33B-parameter transformer producing 4–15 second clips at 24 fps with stereo audio; the open "H3-Base" outputs 768p, and the 2K regeneration module "is not yet open-sourced". [P, repo 28 Oct 2026; S for the release date] — [MiniMax-AI/MiniMax-H3 README](https://github.com/MiniMax-AI/MiniMax-H3/blob/main/README.md); [Comfy docs: MiniMax H3](https://github.com/Comfy-Org/docs/blob/main/tutorials/video/minimax/minimax-h3.mdx); [comfyui-wiki, 3 Aug 2026](https://comfyui-wiki.com/en/news/2026-08-03-minimax-h3-open-weights-comfyui)
- Kandinsky 6.0 Video (3B Lite and 29B Pro, 5-second video with 44 kHz audio, reportedly MIT-licensed) was open-sourced 6 Oct 2026. Official ComfyUI docs and README still list only Kandinsky 5 as of 16–17 Nov 2026. [S for 6.0; P for the ComfyUI observation] — [comfyui-wiki, 6 Oct 2026](https://comfyui-wiki.com/news/2026-10-06-kandinsky-6-0); [creativeainews.com](https://www.creativeainews.com/articles/kandinsky-6-open-audio-video-16gb-gpu-ram-2026/); [ComfyUI README](https://github.com/Comfy-Org/ComfyUI/blob/master/README.md)
- Cross-check: the low-VRAM app WanGP (13 Nov 2026) supports "Wan 2.1/2.2 and derived models, MiniMax H3, LTX-2/2.3/2.5, Hunyuan Video 1/1.5, LongCat, Kandinsky, LTXV, MagiHuman"; ComfyUI's README (17 Nov 2026) lists "Wan 2.1 and 2.2, LTX-Video 2 and 2.3, HunyuanVideo 1.5, Kandinsky 5 Video, CogVideoX, Cosmos Predict2, Bernini-R, SCAIL 2, and Mochi" plus "MiniMax H3 and LTX-AV". Neither lists any Wan newer than 2.2. [P] — [WanGP README](https://github.com/deepbeepmeep/Wan2GP/blob/main/README.md); [ComfyUI README](https://github.com/Comfy-Org/ComfyUI/blob/master/README.md)

**Quality versus closed models**
- A 13 Nov 2026 roundup of the Artificial Analysis arena names MiniMax H3 the best open-weights model, ranked #3 on its text-to-video board (Elo 1161) and "the first open-weights model in the video top tier". [S] — [marktechpost.com, 13 Nov 2026](https://www.marktechpost.com/2026/11/13/best-ai-video-generation-models-2026/)
- An undated snapshot of Artificial Analysis's open-weights image-to-video board shows MiniMax H3 first (Elo 1185), MAGI-2 Preview second (1099) and LTX-2.5 Fast third (1040). [S] — [Artificial Analysis open-weights I2V leaderboard](https://artificialanalysis.ai/video/leaderboard/image-to-video/open-weights)
- Several 2026 reviews rank HunyuanVideo below Wan 2.2 for most users and call Wan the best overall open option with the largest LoRA and tooling community. These lists come mostly from vendors with a stake. [S] — [thundercompute.com](https://www.thundercompute.com/blog/best-open-source-ai-video-generation-models); [morphic.com list](https://morphic.com/resources/list/best-open-source-ai-video-models)

**Licences and regional limits (important for an EU/UK creator)**
- HunyuanVideo 1.5: the licence text says it "DOES NOT APPLY IN THE EUROPEAN UNION, UNITED KINGDOM AND SOUTH KOREA" and forbids using the model or its outputs outside the licensed territory. [P] — [HunyuanVideo-1.5 LICENSE](https://github.com/Tencent-Hunyuan/HunyuanVideo-1.5/blob/main/LICENSE)
- MiniMax H3: ComfyUI's docs say the MiniMax H3 Community License "excludes some regions unless you hold a separate license from MiniMax" and tell users to review its "territorial and commercial-use conditions". Third-party reports name the excluded regions as the US, EU, UK and South Korea (local deployment only; the hosted API is sold worldwide). [P for the existence of exclusions; S for the list] — [Comfy docs: P-H3-Image](https://github.com/Comfy-Org/docs/blob/main/tutorials/image/pruna/p-h3-image.mdx); [Comfy docs: Pika H3 Flex](https://github.com/Comfy-Org/docs/blob/main/tutorials/video/pika/pika-h3-flex.mdx); [mer.vin](https://mer.vin/news/minimax-h3-open-weight-video-model-blocked-us-eu-uk/); [runaihome.com](https://runaihome.com/blog/minimax-h3-open-weights-local-ai-hardware-guide-2026/)
- MiniMax H3: "Commercial use of locally generated outputs requires a MiniMax commercial license, available through Comfy, the only official reseller. Generations on Comfy Cloud already include commercial rights." [P, 16 Nov 2026] — [Comfy docs: MiniMax H3](https://github.com/Comfy-Org/docs/blob/main/tutorials/video/minimax/minimax-h3.mdx)
- LTX-2.5: worldwide LTX-2.x Community License; only entities with annual revenue of at least $10,000,000 must buy a commercial licence. The Hugging Face repository is gated: you must accept the licence and wait for approval before downloads work. [P] — [LTX-2 LICENSE-2_x](https://github.com/Lightricks/LTX-2/blob/main/LICENSE-2_x); [Comfy docs: LTX-2.5](https://github.com/Comfy-Org/docs/blob/main/tutorials/video/ltx/ltx-2-5.mdx)
- Wan 2.2: Apache 2.0, commercial use allowed, no territorial restriction. [P] — [Comfy docs: Wan2.2](https://github.com/Comfy-Org/docs/blob/main/tutorials/video/wan/wan2_2.mdx)

**VRAM and memory**
- Wan 2.2 official reference pipeline: 14B at 720p "can run on a GPU with at least 80GB VRAM" (measured peak 59.8 GB); the 5B model runs on 24 GB (peak 22.9 GB on an RTX 4090). [P] — [Wan2.2 README](https://github.com/Wan-Video/Wan2.2/blob/main/README.md); [official efficiency table](https://github.com/Wan-Video/Wan2.2/blob/main/assets/comp_effic.png)
- In ComfyUI, "the Wan2.2 5B version should fit well on 8GB vram with the ComfyUI native offloading"; the official 14B template uses fp8-scaled weights plus 4-step LightX2V LoRAs. [P] — [Comfy docs: Wan2.2](https://github.com/Comfy-Org/docs/blob/main/tutorials/video/wan/wan2_2.mdx); [official benchmark workflow definition](https://github.com/Comfy-Org/workflow_templates/blob/main/benchmarks/video_wan2_2_14B_t2v.json)
- HunyuanVideo 1.5: official minimum GPU memory 14 GB with model offloading; ComfyUI describes it as running "on consumer GPUs (24GB VRAM)"; native 720p with a super-resolution model for 1080p. [P] — [HunyuanVideo-1.5 README](https://github.com/Tencent-Hunyuan/HunyuanVideo-1.5/blob/main/README.md); [Comfy docs: HunyuanVideo 1.5](https://github.com/Comfy-Org/docs/blob/main/tutorials/video/hunyuan/hunyuan-video-1-5.mdx)
- LTX-2.5: Lightricks reportedly states both "Min VRAM: 16GB" (model page) and "minimum 32GB+ VRAM" with an 80 GB A100/H100 recommended (system requirements page). Community guides say FP8 fits a 32 GB RTX 5090, int8 with CPU offload runs on 24 GB (about 20 GiB resident on an RTX 4090), and a 12 GB test peaked at 45 GB system RAM. [S, third-party guides] — [openclawdc.com](https://openclawdc.com/blog/can-i-run-ltx-2-5-locally/); [runaihome.com](https://runaihome.com/blog/ltx-2-5-local-ai-video-hardware-guide-2026/); [ltxworkflow.com](https://ltxworkflow.com/guide/ltx-2-5-vram-requirements)
- MiniMax H3: figures vary by source — about 123.6 GB in BF16; 24–32 GB GPU plus roughly 75 GB RAM at INT8; ComfyUI's pruned INT8 transformer is about 21 GB and fits a 24 GB card; recipes exist from 12 GB VRAM with weights streamed from 32 GB+ RAM. None is an official MiniMax figure. [S] — [willitrunai.com](https://willitrunai.com/blog/minimax-h3-vram-requirements); [localrigcheck.com](https://localrigcheck.com/minimax-h3/); [openclawdc.com](https://openclawdc.com/blog/can-i-run-minimax-h3-locally/)
- MiniMax's own serving example for H3 uses four GPUs (`--num-gpus 4`). [P] — [MiniMax-H3 README](https://github.com/MiniMax-AI/MiniMax-H3/blob/main/README.md)
- Kandinsky 6.0: reported full-GPU peaks of 72.8 GiB (Pro) and about 44 GiB (Lite); with block offloading both run on 16/24/32 GB cards, the 16 GB preset needing roughly 58 GiB of system RAM. [S] — [creativeainews.com](https://www.creativeainews.com/articles/kandinsky-6-open-audio-video-16gb-gpu-ram-2026/)
- WanGP claims select models run with "as little as 4 GB of VRAM" and supports GTX 10XX and newer NVIDIA cards and AMD RDNA 2–4. [P, vendor claim] — [WanGP README](https://github.com/deepbeepmeep/Wan2GP/blob/main/README.md)
- Download sizes of the official ComfyUI templates: Wan 2.2 14B I2V 38.0 GB; Wan 2.2 5B 18.1 GB; HunyuanVideo 1.5 720p 45.4 GB; LTX-2.5 53.2–61.4 GB; MiniMax H3 44.5–56.9 GB. [P, 17 Nov 2026] — [workflow_templates index.json](https://github.com/Comfy-Org/workflow_templates/blob/main/templates/index.json)

**Generation time for a ~5-second clip**
- Official Wan 2.2 numbers (reference code, no distillation, single GPU): TI2V-5B 720p on an RTX 4090 takes 525–535 s (about 9 minutes); 14B 720p takes 1,042–1,056 s on one H100 and 2,736–2,811 s on one A100; 14B 480p takes about 327 s on an H100. [P] — [official efficiency table](https://github.com/Wan-Video/Wan2.2/blob/main/assets/comp_effic.png)
- Community figures for Wan 2.2 14B at 720p, 5 s: one guide gives about 2:40 on an RTX 4090 and 1:45 on an RTX 5090; another gives about 8 minutes (4090) and 5 minutes (5090) at int8, and 12 versus 7 minutes at FP16. Settings are not comparable. [S] — [dev.to guide A](https://dev.to/thurmon_demich/rtx-5090-vs-4090-for-video-gen-in-2026-32gb-matters-k3i); [dev.to guide B](https://dev.to/runcai/rtx-5090-vs-4090-for-comfyui-wan-benchmarks-vram-and-when-to-rent-cloud-gpu-2fja)
- With 4-step LightX2V distillation, a third-party model card reports 22.5 s (T2V) and 26.7 s (I2V) end to end at 720p on one RTX 5090 (NVFP4 sparse variant, Blackwell GPUs only). [S] — [Hugging Face model card](https://huggingface.co/charles2530/Wan2.2-NVFP4-Sparse)
- Vendor claim: Wan 2.2 14B FP16 on an A100 or H100 takes 3–5 minutes per 5-second 720p clip. Methodology not given. [S, vendor] — [spheron.network](https://www.spheron.network/blog/gpu-cloud-video-ai-2026/)
- HunyuanVideo 1.5: officially, the 480p I2V step-distilled model lets "a single RTX 4090 ... generate videos within 75 seconds". For 720p on a 4090, third-party estimates range from 8–12 minutes to about 22 minutes. [P for 75 s; S for 720p] — [HunyuanVideo-1.5 README](https://github.com/Tencent-Hunyuan/HunyuanVideo-1.5/blob/main/README.md); [vantaige.io](https://vantaige.io/ai-tool/hunyuanvideo); [dev.to](https://dev.to/thurmon_demich/best-gpu-for-hunyuanvideo-ai-video-generation-in-2026-5a30)
- LTX-2.5 in ComfyUI: about 25 s for a 4-second 720p clip on an RTX 5090 (NVFP4) and about 45 s on an RTX 4090 (FP8), from community tables. The headline "10-second clip in 6.8 seconds" is a vendor claim on 2× GB200 hardware, not a consumer card. [S] — [runaihome.com](https://runaihome.com/blog/ltx-2-5-local-ai-video-hardware-guide-2026/); [venturebeat.com](https://venturebeat.com/ai/ltx-2-5-can-generate-a-10-second-ai-video-from-an-image-in-just-6-8-seconds-on-nvidia-superchips-and-its-open-weights/)
- MiniMax H3 on one RTX 5090 (one blogger's series): a 5-second 2K clip (draft plus upscale) in about 174 s with a 32.0 GB peak; 15 seconds of native 1344×768 in 518 s; a 15-second 1080p clip with audio cut from 625 s to 314 s by tuning. On a 24 GB RTX 4090 D, 164–406 s per 1344×768 clip was reported with SGLang. [S] — [ai-muninn.com part 14](https://ai-muninn.com/en/blog/open-h3-regenerate-2k-rtx5090); [part 5](https://ai-muninn.com/en/blog/minimax-h3-rtx5090-config-stack); [part 2](https://ai-muninn.com/en/blog/minimax-h3-rtx5090-speedup-vsr)
- Six-step Pika H3 Flex adapters for H3: "a 5-second 1344x768 clip finishes in about a minute on a single card, instead of the 20 to 50 steps a non-distilled H3 run needs" (card not named). [P, vendor claim relayed by Comfy docs] — [Comfy docs: Pika H3 Flex](https://github.com/Comfy-Org/docs/blob/main/tutorials/video/pika/pika-h3-flex.mdx)

### Inferences
- "Open is close to closed" is true only for MiniMax H3, and only at 768p; its licence makes local use legally awkward for a creator in the EU or UK and requires a paid licence for commercial use of local outputs. For an EU/UK creator the cleanly usable open models are Wan 2.2 (Apache 2.0) and LTX-2.5 (free below $10M revenue).
- The speed that matters is the distilled/quantised community configuration, not the official one: official Wan 2.2 14B at 720p needs an 80 GB card and 17 minutes per clip, while the 4-step ComfyUI setup is one to two orders of magnitude faster on a 24–32 GB card.
- For vertical social clips, 720p native is the practical ceiling for Wan 2.2 and open H3; 1080p means an extra upscale pass (Hunyuan SR, LTX upscaler, RelayVSR/SeedVR2), which adds time and cost.
- Data-centre cards (L40S, A100, H100) are needed for un-quantised weights, not for speed per dollar; a rented RTX 4090/5090 running distilled workflows is the cost-efficient tier.

### Gaps
- No controlled benchmark covering the same workflow on a 24 GB consumer card and a data-centre card was found; all consumer timings are single-source blog or guide figures with differing settings.
- No direct benchmark for Wan 2.2 14B 4-step at 720p on an RTX 4090 (only RTX 5090). No verified Kandinsky 6.0 timings.
- I could not open the Hugging Face model cards or the MiniMax licence text, so the exact list of excluded territories and the reported $20M revenue cap are unconfirmed.
- Whether generating with MiniMax H3 on Comfy Cloud is permitted for users located in excluded regions is not stated in the docs I read.
- Live Artificial Analysis rankings were not opened; the Elo figures are from summaries and an undated snapshot.

## 2. Can anything useful run locally on integrated graphics or CPU only?

### Takeaway
Video generation on ordinary integrated graphics or CPU is not a practical route: the tools technically start, but the vendors themselves call CPU mode a "last resort" and say video is "best on discrete GPUs". Image generation with small distilled models does work on CPU or Intel Arc integrated graphics (about 0.5–36 seconds per 512px image), and only the newest high-memory integrated GPUs (AMD Strix Halo class, Intel Core Ultra Arc) are officially supported for video at all, with no trustworthy speed data found.

### Cited Findings
- ComfyUI supports "CPU - Use the `--cpu` parameter (slower)", and its troubleshooting guide describes it as "CPU mode (very slow but works with any hardware, only use as absolute last resort)". [P, 16 Nov 2026] — [Comfy docs: system requirements](https://github.com/Comfy-Org/docs/blob/main/installation/system_requirements.mdx); [Comfy docs: troubleshooting](https://github.com/Comfy-Org/docs/blob/main/troubleshooting/overview.mdx)
- ComfyUI's supported hardware now includes AMD GPUs on Windows via ROCm 10.0 (RDNA 2, 3, 3.5 and 4) and Intel Arc via native PyTorch `torch.xpu`; portable builds for AMD and Intel GPUs exist. [P] — [Comfy docs: system requirements](https://github.com/Comfy-Org/docs/blob/main/installation/system_requirements.mdx); [ComfyUI README](https://github.com/Comfy-Org/ComfyUI/blob/master/README.md)
- AMD integrated GPUs have official Windows ROCm PyTorch builds: Ryzen AI Max "Strix Halo" (gfx1151), Radeon 890M/880M (gfx1150), Ryzen AI 7 350 (gfx1152), Radeon 820M, Radeon 780M/760M and Radeon 680M. On RDNA 2 and older "attention runs noticeably slower". [P, 13 Nov 2026] — [WanGP AMD installation guide](https://github.com/deepbeepmeep/Wan2GP/blob/main/docs/AMD-INSTALLATION.md)
- ComfyUI v0.40.0 (13 Oct 2026) shipped a speed-up specifically for "AMD gfx1151" (Strix Halo). [P] — [ComfyUI changelog](https://github.com/Comfy-Org/docs/blob/main/changelog/index.mdx)
- Intel's own AI Playground requires an Intel Core Ultra with built-in Arc GPU for its full "Studio" feature set: "If it says 'Intel(R) Graphics,' your system does not have a built-in Intel Arc GPU and does not meet the minimum specifications." A reduced "Essentials" mode (basic chat and basic image generation and editing) runs on "Intel Core Series 3 with 12GB of system memory". [P, repo 28 Oct 2026] — [intel/AI-Playground readme](https://github.com/intel/AI-Playground/blob/main/readme.md)
- Intel on video: presets for LTX-2.3, LTX-Video, Wan 2.2 14B and Wan 2.1 VACE exist, but "Video Generation Mode: Best on workstations and desktops with discrete GPUs" and "best on discrete GPUs or high-memory Core Ultra systems"; 82 GB+ of disk space is recommended. [P, user guide v3.2.0 dated 28 Aug 2026] — [AI Playground Users Guide](https://github.com/intel/AI-Playground/blob/main/AI%20Playground%20Users%20Guide.pdf); [readme](https://github.com/intel/AI-Playground/blob/main/readme.md)
- stable-diffusion.cpp (pure C/C++) supports Wan 2.1/2.2, LTX-2.3/2.5, HunyuanVideo 1.5 and LingBot-Video on CPU (AVX/AVX2/AVX512), Vulkan, OpenCL, SYCL and Metal back ends; it publishes no CPU or integrated-GPU timings. [P, 15 Nov 2026] — [stable-diffusion.cpp README](https://github.com/leejet/stable-diffusion.cpp/blob/master/README.md)
- Image generation on CPU (FastSD CPU, OpenVINO, Core i7-12700): 0.82 s for a 512×512 image with a 1-step SDXS model; 6.3 s for a 768×768 SDXL 1-step image; about 36 s for a 512×512 FLUX.3 Image Klein image at 4 steps (int4, 8–9 GB RAM), about 72 s for an edit. Minimum RAM 2–8.4 GB depending on model. [P, 6 Nov 2026] — [FastSD CPU readme](https://github.com/rupeshs/fastsdcpu/blob/main/Readme.md)
- Image generation on an Intel Arc integrated GPU (FastSD benchmark): SD Turbo 512×512, 1 step, 1.546 s average, 0.466 s with the tiny decoder. [P] — [FastSD CPU Arc iGPU benchmark](https://github.com/rupeshs/fastsdcpu/blob/main/docs/images/ARCGPU.png)
- Upscaling: Upscayl (Real-ESRGAN on Vulkan) says "Many iGPUs (integrated graphics) do not work but, no harm in trying" and "Upscayl won't work with most iGPUs or CPUs". [P, repo last commit 27 Mar 2026 — older than mid-2026] — [Upscayl README](https://github.com/upscayl/upscayl/blob/main/README.md)
- For low-VRAM dedicated cards (not integrated): Wan 2.2 5B fits 8 GB VRAM in ComfyUI; WanGP claims 4 GB VRAM for select models and 6 GB for HunyuanVideo 1.5. [P, vendor claims] — [Comfy docs: Wan2.2](https://github.com/Comfy-Org/docs/blob/main/tutorials/video/wan/wan2_2.mdx); [WanGP README](https://github.com/deepbeepmeep/Wan2GP/blob/main/README.md); [HunyuanVideo-1.5 README](https://github.com/Tencent-Hunyuan/HunyuanVideo-1.5/blob/main/README.md)

### Inferences
- A typical "weak PC with integrated graphics" (Intel UHD/Iris Xe or older AMD Vega/Radeon 600M-class, 8–16 GB RAM) cannot do useful video generation: the smallest current video template downloads 18 GB of weights and expects 8 GB of dedicated VRAM, and the models' text encoders alone exceed such a machine's memory.
- What such a PC can realistically do locally: still images with distilled models (seconds to about a minute each), light editing, and assembling clips in an editor. Local upscaling and frame interpolation are hit-and-miss on integrated graphics.
- New high-memory integrated GPUs (Strix Halo with 64–128 GB shared memory) change the "will it load" question but not the speed question; buying one for this purpose is a hardware purchase, not a use of the existing PC.

### Gaps
- No benchmark or user report was retrieved for video generation on any integrated GPU (Strix Halo, Radeon 890M, Intel Arc 140V/B390 or Apple-class shared memory). This is the largest evidence hole in this question.
- No source retrieved on frame interpolation (RIFE/Flowframes) performance on integrated graphics. [U] ncnn-Vulkan builds of RIFE and Real-ESRGAN have historically run on Intel/AMD integrated GPUs with Vulkan, slowly; not re-verified.
- Reddit user reports could not be searched.

## 3. Raw GPU rental: hourly prices and cost per 5-second clip including overhead

### Takeaway
In November 2026 a rented 24–32 GB card costs roughly $0.25–$0.50 per hour on marketplaces (Vast.ai, RunPod Community Cloud, older workstation cards) and $0.89–$1.19 per hour for an RTX 4090/5090 on RunPod Secure Cloud; prices have been rising, not falling. Pure compute is about $0.01–$0.12 per 5-second clip, but storage ($4–$7 a month for the models), start-up time, idle time and rejected takes push a realistic light-use figure to roughly $0.10 per generation and $0.30–$0.60 per finished clip.

### Cited Findings

**Hourly prices**
- RunPod Secure Cloud on-demand, from RunPod's API as captured by SkyPilot's catalog bot on 10 Nov 2026 (unchanged since at least 23 Oct): RTX 4090 $0.89; RTX 5090 $1.19; RTX 3090 $0.50; RTX A5000 24 GB $0.27; RTX 4000 Ada 20 GB $0.28; RTX A4000 16 GB $0.25; RTX A6000 48 GB $0.59; A40 48 GB $0.59; L40S $1.09; A100 80 GB $1.79; H100 $2.89; RTX PRO 6000 96 GB $2.49. [P for the catalog file; it is an automated copy of provider data] — [SkyPilot catalog: runpod/vms.csv](https://github.com/skypilot-org/skypilot-catalog/blob/master/catalogs/v8/runpod/vms.csv)
- Conflict: RunPod's own pricing page as summarised in July 2026 listed the RTX 4090 "from $0.34", the RTX 5090 "from $0.69", the L40S from $0.79 and the A40 at $0.35; trackers earlier in 2026 quoted the 4090 at $0.34 (Community Cloud) and $0.69 (Secure Cloud). The November catalog shows only Secure Cloud and is higher. [S] — [runpod.io/pricing](https://www.runpod.io/pricing); [computeprices.com](https://computeprices.com/providers/runpod/gpus/rtx4090)
- RunPod has retired spot/interruptible Pods ("The APIs stopped accepting bids") and deprecated savings plans; only on-demand remains. Community Cloud still exists but its Pods "aren't guaranteed a public IP address". [P, 16 Nov 2026] — [RunPod docs: Terraform migration](https://github.com/runpod/docs/blob/main/integrations/terraform/migration.mdx); [RunPod docs: pricing](https://github.com/runpod/docs/blob/main/pods/pricing.mdx); [RunPod docs: runpodctl pod](https://github.com/runpod/docs/blob/main/runpodctl/reference/runpodctl-pod.mdx)
- Vast.ai (marketplace; prices float): RTX 4090 medians of about $0.31–$0.52 per hour across trackers, advertised floor "from $0.13"; RTX 5090 median $0.78 on 10 Nov 2026 with hosts from $0.49 to $1.12, other trackers $0.40–$0.64. Storage and bandwidth are billed separately. [S] — [findstack.com](https://findstack.com/resources/runpod-vs-vast-ai); [computeprices.com, 5 Aug 2026](https://computeprices.com/providers/vast/gpus/rtx4090); [thundercompute.com, 10 Nov 2026](https://www.thundercompute.com/blog/nvidia-rtx-5090-pricing); [costbench.com](https://www.costbench.com/software/ai-gpu-cloud/vast-ai/)
- Lambda on-demand, from Lambda's API via SkyPilot's bot on 17 Nov 2026: Quadro RTX 6000 24 GB $0.69; A6000 48 GB $1.09; A10 24 GB $1.29; A100 $1.99; GH200 $2.59; H100 PCIe $3.79; H100 SXM $4.89; B200 $7.99. Lambda offers no consumer RTX cards. [P for the catalog file] — [SkyPilot catalog: lambda/vms.csv](https://github.com/skypilot-org/skypilot-catalog/blob/master/catalogs/v8/lambda/vms.csv)
- Lambda prices rose within four weeks: between the 23 Oct and 17 Nov 2026 catalog versions the H100 PCIe went from $3.29 to $3.79, the H100 SXM from $4.29 to $4.89 and the GH200 from $2.29 to $2.59. Third-party trackers still show older, lower Lambda figures (A10 $0.86, A6000 $0.80–$0.92, H100 PCIe $2.49–$2.86). [P for history; S for trackers] — [SkyPilot catalog history](https://github.com/skypilot-org/skypilot-catalog/commits/master/catalogs/v8/lambda/vms.csv); [costbench.com](https://costbench.com/software/ai-gpu-cloud/lambda-labs/)
- AWS on-demand Linux (catalog updated 17 Nov 2026): g4dn.xlarge (T4 16 GB) $0.526/h in us-east-1 and $0.658/h in Frankfurt; g5.xlarge (A10G 24 GB) $1.006 and $1.258; g6.xlarge (L4 24 GB) $0.805 and $1.006; g6e.xlarge (L40S 48 GB) $1.861 and $2.327. [P for the catalog file] — [SkyPilot catalog: aws/vms.csv](https://github.com/skypilot-org/skypilot-catalog/blob/master/catalogs/v8/aws/vms.csv)

**Overhead and hidden costs (RunPod official docs, 16 Nov 2026)**
- Storage: container disk $0.10/GB/month while running; volume disk $0.10/GB/month running and $0.20/GB/month while the Pod is stopped; network volume $0.07/GB/month under 1 TB. Compute and storage are billed per second; no data ingress or egress fees. [P] — [RunPod docs: pricing](https://github.com/runpod/docs/blob/main/pods/pricing.mdx)
- "You must have at least one hour's worth of credits for your selected configuration to deploy"; Pods stop when the balance reaches $0 and Pods without a network volume are terminated with data lost. The ComfyUI tutorial asks for "at least $10 in Runpod credits". [P] — [RunPod docs: pricing](https://github.com/runpod/docs/blob/main/pods/pricing.mdx); [RunPod docs: ComfyUI tutorial](https://github.com/runpod/docs/blob/main/tutorials/pods/comfyui.mdx)
- Start-up: "The Pod can take up to 30 minutes to initialize the container and start the ComfyUI HTTP service" on first deployment; later starts are faster; allow 2–3 minutes for the web service. The official template "doesn't come pre-installed with any models". [P] — [RunPod docs: ComfyUI tutorial](https://github.com/runpod/docs/blob/main/tutorials/pods/comfyui.mdx)
- Model downloads per workflow are 18–61 GB (see question 1). [P] — [workflow_templates index.json](https://github.com/Comfy-Org/workflow_templates/blob/main/templates/index.json)

### Inferences
- Pure compute per ~5-second 720p clip, combining the hourly rates above with the reported timings in question 1 (my arithmetic):
  - LTX-2.5 distilled: about $0.011 on a 4090 at $0.89/h (45 s) or $0.008 on a 5090 at $1.19/h (25 s).
  - Wan 2.2 14B with the 4-step LoRA on a 5090 (23–27 s): about $0.007–$0.009.
  - Wan 2.2 14B quantised without distillation on a 4090 (2:40 to 8 minutes): $0.04–$0.12.
  - MiniMax H3 5-second clip with 2K upscale on a 5090 (174 s): about $0.06.
  - HunyuanVideo 1.5 at 720p on a 4090 (8–22 minutes): $0.12–$0.33.
  - Official un-distilled Wan 2.2 14B at 720p on one H100 at $2.89/h (1,042 s): $0.84 — more than the per-clip APIs charge.
- Realistic monthly example for a light user (assumptions: 30 finished clips, 4 attempts each, 60 s per attempt, GPU busy 40% of billed time, eight sessions with 5 minutes of start-up, 80 GB network volume, RunPod Secure 4090): about 5.7 billed hours × $0.89 = $5.07, plus $5.60 storage = roughly $10.70 a month, or about $0.09 per generation and $0.36 per finished clip. On a marketplace 4090 at about $0.40/h the compute part halves.
- The cost trap is not the GPU rate but leaving things on: a stopped Pod with a 100 GB volume disk costs $20 a month doing nothing, and an idle running 4090 costs about $21 a day.
- With spot Pods retired and Secure prices up, the "$0.34 per hour 4090" that most 2026 guides quote should be treated as a Community-Cloud best case, not a planning number.

### Gaps
- RunPod Community Cloud prices for November 2026, and Vast.ai's live prices and storage rates, were not verified on the vendors' pages.
- TensorDock, Thunder Compute, Hyperstack, Salad and other "comparable providers" were not researched.
- Whether the SkyPilot RunPod figures exactly match what the RunPod console shows to a retail user today was not cross-checked.

## 4. Managed ComfyUI clouds and free GPU options

### Takeaway
The official Comfy Cloud is the most beginner-friendly "rent compute" route: $20 a month buys about 4.4 hours of a 96 GB RTX PRO 6000 with every current open model pre-installed and billing only while a workflow runs, which is a few hundred fast 5-second clips. Third-party hosts (RunComfy, ThinkDiffusion, MimicPC, RunningHub) rent a full ComfyUI machine by the hour for roughly $0.30–$3 per hour with more freedom and more ways to waste money; free GPUs (Kaggle, Colab, Lightning) are workable only for small models and patient tinkerers.

### Cited Findings

**Comfy Cloud (official)**
- Runs on "Blackwell RTX 6000 Pros"; "No technical knowledge required"; all models and custom nodes pre-installed; every official template is ready to run, including Wan 2.2, LTX-2.5 and MiniMax H3. [P, 16 Nov 2026; "no technical knowledge" is a vendor claim] — [Comfy docs: Comfy Cloud](https://github.com/Comfy-Org/docs/blob/main/get_started/cloud.mdx)
- Plans: Standard $20/month (4,200 credits), Creator $35 (7,400), Pro $100 (21,100), Team $700 (147,700); yearly billing $16/$28/$80/$630 per month. [S, pricing page not opened] — [comfy.org/cloud/pricing](https://www.comfy.org/cloud/pricing); [aisotools.com](https://aisotools.com/comfyui-pricing)
- GPU time costs 0.266 credits per second on the `rtx_pro_6000`, and 211 credits = $1. A third-party site quotes 0.39 credits per second, which conflicts with the official docs. [P] — [Comfy docs: partner node pricing, Cloud GPU table](https://github.com/Comfy-Org/docs/blob/main/tutorials/partner-nodes/pricing.mdx); contradicted by [scopeful.org](https://www.scopeful.org/tools/comfyui-cloud)
- "Cloud sessions only bill you while the GPU is actively running." [P] — [Comfy docs: Comfy Cloud](https://github.com/Comfy-Org/docs/blob/main/get_started/cloud.mdx)
- Limits: maximum runtime per workflow 30 minutes (Standard, Creator) or 1 hour (Pro); one workflow at a time in the UI; a fixed set of custom nodes ("You cannot install your own node packs"); importing your own models or LoRAs from Civitai or Hugging Face requires Creator or higher. [P] — [Comfy docs: Comfy Cloud](https://github.com/Comfy-Org/docs/blob/main/get_started/cloud.mdx); [Comfy docs: import models](https://github.com/Comfy-Org/docs/blob/main/cloud/import-models.mdx)
- Free allowance: "new users get 5 free runs"; a paid plan is needed to run workflows after that. A third-party site instead lists 400 free credits a month; the official docs do not say that. [P] — [Comfy docs: MCP page](https://github.com/Comfy-Org/docs/blob/main/agent-tools/mcp.mdx); [Comfy docs: subscribing](https://github.com/Comfy-Org/docs/blob/main/support/subscription/subscribing.mdx)
- Monthly plan credits reset each cycle; top-up credits last one year; plans auto-renew. [S] — [Comfy support: how credits work](https://support.comfy.org/articles/5846341390-how-credits-work-in-comfy)
- One reviewer estimates "a five-second video uses roughly 11 credits". [S, third-party] — [aisotools.com](https://aisotools.com/comfyui-pricing)

**Other managed ComfyUI hosts (all from search summaries; vendor pages not opened)**
- RunComfy (billed per second on GPU uptime; pay-as-you-go versus Pro-subscriber hourly rates): 16 GB (T4/A4000) $0.99 / $0.79; 24 GB (A10G/A5000) $1.75 / $1.39; 48 GB A6000 $2.50 / $1.99; 48 GB L40S $2.99 / $2.15; A100 80 GB $4.99 / $3.99; H100 $7.49 / $5.99. Pro reportedly includes 200 GB storage and a $10 monthly credit. The Pro subscription price was not found. [S] — [RunComfy billing docs](https://docs.runcomfy.com/serverless/about-billing); [RunComfy guide](https://comfyui-guides.runcomfy.com/ultimate-comfyui-how-tos-a-runcomfy-guide/what-plans-do-you-have)
- ThinkDiffusion: pay-as-you-go machines at roughly $0.59–$1.99 per hour across three tiers; TD-Pro $29.99/month ($19.99 billed annually) adds persistent storage and 20% off machine rates. Figures come from third-party snapshots dated May–November 2026. [S] — [wireflow.ai](https://www.wireflow.ai/blog/best-comfyui-cloud-pricing-tools-in-2026); [xpay.sh](https://www.xpay.sh/saas-pricing/think-diffusion)
- MimicPC: hourly rental from $0.29–$0.49 (T4) to $1.99 (L40S); an "Essential" plan at $6.98 for the first month (renews $13.95) with $12 of credit and 50–100 GB storage (sources disagree); short free trial; orders reported as non-refundable. [S] — [aisotools.com](https://aisotools.com/pricing/mimicpc); [sourceforge.net](https://sourceforge.net/software/product/MimicPC); [dealify.com](https://dealify.com/mimicpc)
- RunningHub: free account with 100 RH Coins plus daily bonus coins usable on open-source workflows (Qwen, Wan, LTX, Flux); paid "Creative Member" plans from $8.90 to $25.90 per month; metered at 0.2 RH coins per second on 24 GB VRAM and 0.4 on 48 GB; watermark removal requires a subscription. [S] — [RunningHub post](https://www.runninghub.ai/post/2026113437813710850); [blog-ia.com](https://blog-ia.com/rtcl_listing/runninghub/)

**Free GPU options (third-party sources only)**
- Kaggle: about 30 GPU-hours a week (community-reported; Kaggle's docs give no number and the quota floats), on a P100 16 GB or two T4s, with 9–12 hour sessions. [S] — [gpuperhour.com](https://gpuperhour.com/blog/free-cloud-gpus-and-credits); [agentdeals.dev](https://agentdeals.dev/vendor/kaggle)
- Google Colab: free T4 sessions up to 12 hours with a 90-minute idle timeout and no availability guarantee; Colab Pro $9.99/month for 100 compute units (a T4 burns about 1.2–1.8 units per hour); pay-as-you-go 100 units for $9.99. Remote desktops and bypassing the notebook interface are described as poor fits for free Colab. [S] — [gpuperhour.com](https://gpuperhour.com/blog/google-colab-alternatives); [aitoolsatlas.ai](https://aitoolsatlas.ai/tools/google-colab/pricing)
- Lightning AI: free plan with 15 credits a month; sources disagree on what that buys (about 22 T4 hours versus about 80 spot hours); Lightning says free grants can change at any time. [S] — [Lightning billing FAQ](https://lightning.ai/docs/platform/overview/faq/billing.md); [usagepricing.com](https://usagepricing.com/blueprint/lightning-ai)

### Inferences
- Comfy Cloud arithmetic (mine): Standard's 4,200 credits ÷ 0.266 = 15,789 GPU-seconds, about 4.4 hours a month; Creator about 7.7 hours; Pro about 22 hours. That is an effective $4.54 per GPU-hour, versus $2.49 for the same card rented raw on RunPod — the premium buys zero set-up and no idle billing.
- Cost per clip on Comfy Cloud Standard: $0.0013 per GPU-second, so a 40-second distilled run is about $0.05, a 2-minute run $0.15 and a 5-minute high-quality run $0.38. At 60 seconds per attempt, $20 covers about 260 attempts.
- For the target user, Standard has two snags: no LoRA or custom-model import (a 3D-cartoon style LoRA needs the $35 Creator plan) and the 30-minute cap, which matters only for long or upscaled jobs.
- Hour-metered hosts (RunComfy, ThinkDiffusion, MimicPC) bill while the machine is up, so thinking time is paid time; they suit long sessions with custom nodes, not occasional clips.
- Free tiers: a 16 GB T4/P100 can run Wan 2.2 5B (8 GB VRAM class) and heavily quantised 14B variants, slowly, with 18–40 GB of models re-downloaded each session. Realistic for learning, not for dependable posting.

### Gaps
- None of the third-party hosts' pricing pages were opened; all figures need confirmation, especially RunComfy's Pro price and whether the listed rates apply to its interactive ComfyUI product as well as its serverless API.
- RunningHub's dollar price per RH coin, regional restrictions and commercial terms were not found.
- Whether Kaggle's and Colab's current terms allow running a ComfyUI web interface through a tunnel was not verified. [U] Colab's free tier has restricted Stable-Diffusion-style web UIs since 2023.
- Other hosts current in November 2026 (for example InstaSD, Floyo, RunDiffusion, SeaArt, Tensor.art) were not researched.

## 5. Learning curve: hours to a good clip, and what goes wrong

### Takeaway
On Comfy Cloud a beginner can plausibly get a first clip in well under an hour by opening a template and typing a prompt; on a self-managed rented GPU the first session is closer to one to three hours and consistent "good" results take days of practice, though no measured data on this was found. The official documentation's own list of common failures is missing models, custom-node conflicts, out-of-memory errors and driver or version mismatches.

### Cited Findings
- Comfy's own comparison: Cloud needs "No technical knowledge required", while self-hosted means "you'll need to troubleshoot custom node installations and local installation issues". [P, vendor statement] — [Comfy docs: Comfy Cloud](https://github.com/Comfy-Org/docs/blob/main/get_started/cloud.mdx)
- Comfy Cloud's first-run flow is five steps: pick a template, open it, edit the prompt or input image, click Run, download the video. [P] — [Comfy docs: Comfy Cloud](https://github.com/Comfy-Org/docs/blob/main/get_started/cloud.mdx)
- Official ComfyUI troubleshooting topics: ComfyUI won't start (drivers, requirements); "Prompt execution failed" (custom nodes, model files, VRAM); slow performance and out-of-memory; model architecture mismatch; missing models; model loading errors. Custom-node faults are diagnosed by disabling all nodes and binary-searching. [P] — [Comfy docs: troubleshooting](https://github.com/Comfy-Org/docs/blob/main/troubleshooting/overview.mdx); [custom node issues](https://github.com/Comfy-Org/docs/blob/main/troubleshooting/custom-node-issues.mdx); [model issues](https://github.com/Comfy-Org/docs/blob/main/troubleshooting/model-issues.mdx)
- On a rented Pod the user must deploy a template, wait up to 30 minutes on first start, then install each missing model through ComfyUI Manager because the template ships without models; a "Bad Gateway" error on first connection is expected for 2–3 minutes. [P] — [RunPod docs: ComfyUI tutorial](https://github.com/runpod/docs/blob/main/tutorials/pods/comfyui.mdx)
- Model access can itself block a beginner: LTX-2.5 downloads "will fail without access" until a gated Hugging Face request is approved. [P] — [Comfy docs: LTX-2.5](https://github.com/Comfy-Org/docs/blob/main/tutorials/video/ltx/ltx-2-5.mdx)
- Some workflows need extra node packs (for example Wan 2.2 Animate needs three custom node packs; LTX-2.5 DFR needs ComfyUI-LTXVideo), which Comfy Cloud may or may not include. [P] — [workflow_templates index.json](https://github.com/Comfy-Org/workflow_templates/blob/main/templates/index.json)
- A 2026 tutorial advertises a local Wan 2.2 set-up as "13 steps, 60 min". [S, title only] — [tech-insider.org](https://tech-insider.org/?p=44797)

### Inferences
- My estimate (not measured): Comfy Cloud, 20–60 minutes to a first clip and 3–6 hours to learn prompting, image-to-video and aspect-ratio settings well enough for consistent output; raw GPU rental, 1–3 hours to a first clip and 10–20 hours before the workflow is dependable, because the user also has to learn storage, model folders, node management and shutting the machine down.
- The skills that determine "professional-looking" are the same as on hosted generators (a strong first frame, short motion prompts, several takes); ComfyUI adds an operations burden on top without adding quality for a beginner.

### Gaps
- No user surveys, Reddit threads or timed studies of the beginner learning curve were retrieved; the hour estimates above are mine.
- No frequency data on which errors are most common; the list reflects how the official docs organise their troubleshooting, not incident counts.

## 6. Pay-per-clip APIs for the same open models, and the break-even against renting

### Takeaway
The same open models are sold per clip for about $0.05–$0.11 (Replicate's optimised Wan 2.2) up to $0.30–$0.65 (RunPod endpoints, fal, Comfy partner nodes) per 5 seconds, with no set-up. Against the cheapest of these, renting a GPU only wins above roughly 90–100 generations a month, and only if the creator's time is valued at zero; against fal-level prices the break-even is about 15 generations.

### Cited Findings
- Replicate, Wan 2.2 (launch-period blog; current page not opened): fast image-to-video or text-to-video at 480p $0.05 per video; fast text-to-video at 720p $0.10; a co-branded table gives 720p image-to-video at $0.11 per 5-second video; non-optimised image-to-video $0.40 (480p) and $1.00 (720p). [S — published around July–August 2025, older than mid-2026] — [replicate.com/blog/wan-22](https://replicate.com/blog/wan-22); [pruna.ai](https://www.pruna.ai/blog/wan-2-2-video-juiced-fastest-and-cheapest-video-generation)
- RunPod Public Endpoints (official docs, 16 Nov 2026): Wan 2.2 I2V at 720p $0.30 per 5 seconds; Wan 2.2 I2V with LoRA $0.35 per 5 s and $0.56 per 8 s; Wan 2.1 I2V 720p $0.30 per 5 s. [P] — [RunPod docs: public endpoints reference](https://github.com/runpod/docs/blob/main/public-endpoints/reference.mdx)
- fal.ai: Wan 2.2 A14B $0.08–$0.10 per second (sources differ); LTX-2.5 Fast $0.09/s at 720p, $0.13/s at 1080p, $0.19/s at 1440p, $0.30/s at 4K with audio; MiniMax H3 $0.05/s at 480p and $0.06/s at 768p according to a secondary table. [S] — [fal.ai LTX-2.5 Fast page](https://fal.ai/models/lightricks/ltx-2.5/text-to-video/fast); [fal.ai guide](https://fal.ai/learn/tools/ai-video-generators); [costgoat.com](https://costgoat.com/pricing/wan-video)
- Baseline via ComfyUI partner nodes (official docs; 211 credits = $1): LTX-2.5 Fast 27.16 credits/s at 720p and 39.22 at 1080p; LTX-2.5 Pro 36.21 and 51.29; MiniMax H3 27.16 credits/s at 768p and 39.22 at 2K; hosted Wan 2.7 21.1 credits/s at 720p and 31.65 at 1080p; hosted Wan 3.0 30.17 at 720p and 60.35 at 1080p. [P, 16 Nov 2026] — [Comfy docs: partner node pricing](https://github.com/Comfy-Org/docs/blob/main/tutorials/partner-nodes/pricing.mdx)

### Inferences
- Converted to dollars per 5-second clip (my arithmetic): Replicate fast Wan 2.2 $0.05 (480p) to $0.11 (720p); RunPod endpoint Wan 2.2 $0.30; fal Wan 2.2 $0.40–$0.50; fal LTX-2.5 Fast $0.45 (720p) or $0.65 (1080p); fal MiniMax H3 $0.25–$0.30; via Comfy partner nodes LTX-2.5 Fast $0.64 (720p), MiniMax H3 $0.64 (768p), hosted Wan 2.7 $0.50 (720p) and $0.75 (1080p), hosted Wan 3.0 $0.72 (720p) and $1.43 (1080p).
- Break-even model: rented Pod cost ≈ fixed storage (about $6/month) + $0.037 per generation (60 s of compute at 40% utilisation on a $0.89/h card). Break-even generations per month = $6 ÷ (API price − $0.037):
  - versus fal Wan 2.2 at $0.45: about 15 generations;
  - versus RunPod's endpoint at $0.30: about 23;
  - versus Replicate fast 720p at $0.105: about 90;
  - versus Replicate fast 480p at $0.05: about 460.
- If each generation takes 160 s instead of 60 s (non-distilled), rental costs about $0.10 per generation and never beats Replicate's fast endpoint.
- At four attempts per finished clip, 90 generations is only about 23 finished clips a month, so a creator posting daily could save a few dollars a month by renting — at the price of running their own infrastructure.
- Comfy Cloud at $20 flat becomes cheaper than $0.105 per clip above about 190 generations a month, and cheaper than fal-priced clips above about 45.

### Gaps
- Current Replicate and fal prices were not confirmed on the vendors' live pages; the Replicate figures date from the 2025 launch.
- Replicate/fal prices for HunyuanVideo 1.5 and Kandinsky 6.0 were not found.
- WaveSpeed, Atlas Cloud, DeepInfra, Segmind and other resellers of open models were not researched.

## 7. 3D software on rented compute: render farms and cloud workstations

### Takeaway
This question is largely unanswered: no searches could be run on SheepIt, Fox Renderfarm, GarageFarm, RebusFarm, Shadow PC, Vagon or AirGPU, so their November 2026 status and prices are unverified. The only verified numbers are raw cloud GPU rates, which put the compute for a 10–30-second 1080p Blender animation at roughly $0.30 to $13 depending on scene weight (on my assumed frame times), and an AWS GPU workstation at $0.53–$1.26 per hour before Windows licence and storage.

### Cited Findings
- AWS GPU instances usable as cloud workstations (Linux on-demand, 17 Nov 2026): g4dn.xlarge with a T4 16 GB $0.526/h (us-east-1) or $0.658/h (Frankfurt); g5.xlarge with an A10G 24 GB $1.006 or $1.258; g6.xlarge with an L4 24 GB $0.805 or $1.006. Spot prices for g4dn.xlarge were $0.21–$0.35/h. [P for the catalog file] — [SkyPilot catalog: aws/vms.csv](https://github.com/skypilot-org/skypilot-catalog/blob/master/catalogs/v8/aws/vms.csv)
- Azure: NC4as_T4_v3 (T4) $0.526/h and NV36ads_A10_v5 (full A10) $3.20/h in East US. [P; file last touched 26 Oct 2026, underlying price date unknown] — [SkyPilot catalog: azure/vms.csv](https://github.com/skypilot-org/skypilot-catalog/blob/master/catalogs/v8/azure/vms.csv)
- Paperspace machine types still appear in SkyPilot's catalog (P4000 $0.51/h, A4000 $0.76/h, A100-80G $3.18/h, H100 $5.95/h), but the file's last real update could not be dated and it says nothing about whether Paperspace's Windows desktop product still exists. [P for the file; freshness unknown] — [SkyPilot catalog: paperspace/vms.csv](https://github.com/skypilot-org/skypilot-catalog/blob/master/catalogs/v8/paperspace/vms.csv)
- Raw GPU rates that could run Blender Cycles headless: RTX 4090 at $0.89/h (RunPod Secure) or about $0.31–$0.52/h (Vast.ai medians). [P/S, see question 3] — [SkyPilot catalog: runpod/vms.csv](https://github.com/skypilot-org/skypilot-catalog/blob/master/catalogs/v8/runpod/vms.csv); [findstack.com](https://findstack.com/resources/runpod-vs-vast-ai)

### Inferences
- Render cost estimate (assumptions are mine and unverified): a 10–30-second clip at 24–30 fps is 240–900 frames. At 10–60 seconds per 1080p Cycles frame on an RTX 4090 that is 0.7–15 GPU-hours, or about $0.30–$13 at $0.40–$0.89 per hour; Eevee would be several times cheaper. Commercial farms charge more per GPU-hour but finish in minutes by running many nodes in parallel.
- Render farms and cloud PCs solve only the last step. The creator still has to model, light and animate in Blender or Unreal, which on integrated graphics means a sluggish viewport locally or working inside a streamed desktop. For "fast and cheap social clips" by a non-3D-artist this is the slowest route of all; it suits people who already know Blender.
- A DIY AWS workstation at 20 hours a month costs about $10–$25 in compute plus storage and a Windows licence, and requires remote-desktop set-up; flat-fee cloud PCs trade a higher fixed price for simplicity.

### Gaps
- SheepIt, Fox Renderfarm, GarageFarm and RebusFarm: operating status, current prices, trial credits and Blender version support were NOT verified. [U] As of 2025 SheepIt was a free, points-based community farm for Blender (you earn priority by rendering for others, which a weak PC does poorly), and the three commercial farms priced by core-hour, GHz-hour or OctaneBench-hour with trial credits in the $20–$50 range.
- Shadow PC, Vagon and AirGPU: plans, prices, hardware and country availability were NOT verified. [U] Shadow historically sold monthly plans around $30–$50 in selected North American and European countries; Vagon and AirGPU billed by the hour (roughly $0.65–$2+) plus storage.
- No data retrieved on usability over a home connection. [U] Cloud desktops generally want a stable 15–50 Mbps and low latency; colour-critical and high-frame-rate work suffers first.
- No measured per-frame render times for representative social-video scenes; the cost range above rests on my assumed frame times.

## 8. Hardware economics in late 2026: buy instead of rent?

### Takeaway
Current (November 2026) retail prices for GPUs, memory, eGPU enclosures and budget desktops could not be verified, so the buy-versus-rent conclusion rests on mid-2025 reference prices and on the verified fact that cloud GPU prices are rising. Even on optimistic 2025 prices, a 16 GB card equals roughly 20–45 months of the $10–$20 a month that a light cloud user would spend, and it would still be slower than a rented 4090/5090 and would need 32–64 GB of system RAM.

### Cited Findings
- Reference prices from a PCPartPicker data dump (repo last commit 23 Jul 2025 — far older than mid-2026, use only as a pre-shortage baseline): lowest listings were RTX 5060 8 GB $300; RTX 5060 Ti 16 GB $428; RX 9060 XT 16 GB $350; Arc B580 12 GB $260; RTX 5070 12 GB $550; RTX 3060 12 GB $257; RTX 5090 $2,000 (median listing $3,050); DDR5 2×16 GB kits from $70 (median $120) and 2×32 GB from $131 (median $203). [P, old] — [docyx/pc-part-dataset](https://github.com/docyx/pc-part-dataset)
- Memory needs of the current models when run on small cards: about 75 GB RAM for MiniMax H3 at INT8; 45 GB RAM peak for LTX-2.5 on a 12 GB card; about 58 GiB RAM for Kandinsky 6.0 Pro on a 16 GB card. [S] — [willitrunai.com](https://willitrunai.com/blog/minimax-h3-vram-requirements); [openclawdc.com](https://openclawdc.com/blog/can-i-run-ltx-2-5-locally/); [creativeainews.com](https://www.creativeainews.com/articles/kandinsky-6-open-audio-video-16gb-gpu-ram-2026/)
- Signal of tight GPU supply in late 2026: Lambda raised H100 and GH200 hourly prices by 13–15% between 23 Oct and 17 Nov 2026, and RunPod's Secure Cloud RTX 4090 sits at $0.89/h against $0.69/h quoted earlier in 2026. [P] — [SkyPilot catalog: lambda](https://github.com/skypilot-org/skypilot-catalog/blob/master/catalogs/v8/lambda/vms.csv); [SkyPilot catalog: runpod](https://github.com/skypilot-org/skypilot-catalog/blob/master/catalogs/v8/runpod/vms.csv)
- A local Intel route needs at least an Arc discrete card with 8 GB VRAM or a Core Ultra with built-in Arc, plus 82 GB+ of disk. [P] — [intel/AI-Playground readme](https://github.com/intel/AI-Playground/blob/main/readme.md)

### Inferences
- Months of cloud spending equal to a purchase (my arithmetic on the 2025 baseline; real November 2026 prices are probably higher):
  - 16 GB GPU alone at $428 (only if the PC is a desktop with a free slot and adequate power supply): 43 months at $10/month of GPU rental, 21 months at Comfy Cloud Standard's $20, 12 months at Creator's $35.
  - GPU plus 64 GB of RAM (about $560 on 2025 prices): 28–56 months at $10–$20.
  - If the PC is a laptop, or a small desktop that cannot take a card, the options are an external GPU enclosure (needs Thunderbolt, USB4 or OCuLink, which many budget machines lack) or a whole new desktop — roughly double or triple the outlay, pushing break-even to several years.
- A purchase only pays back for heavy use: at 50 GPU-hours a month ($44.50 on a rented 4090 at $0.89/h) a $430–$600 card pays for itself in about 10–14 months, but a 16 GB card runs today's 22–33B models only in quantised, RAM-hungry, slower configurations.
- For a creator who prioritises low cost and speed, buying hardware in late 2026 is not the sensible first move: it front-loads hundreds of dollars, adds a set-up project, and bets on models whose memory appetite has grown every release.

### Gaps
- No verified November 2026 prices for entry-level or used GPUs, DDR5 memory, eGPU enclosures, budget desktops or mini-PCs; no 2026 press coverage of GPU and memory price trends was retrieved. [U] From late 2025 a DRAM shortage pushed DDR5 kit prices to two to three times their mid-2025 level and put upward pressure on graphics-card prices in 2026; 2025 launch MSRPs were $299 (RTX 5060), $429 (RTX 5060 Ti 16 GB), $349 (RX 9060 XT 16 GB) and $249 (Arc B580).
- [U] eGPU enclosures and docks historically cost about $100–$400 before the card and sometimes a power supply; Strix Halo mini-PCs with 64–128 GB started around $1,100–$2,000 in 2025. Not re-verified.
- Electricity cost and resale value were not modelled.

## 9. Bottom line: who should take this route, and for whom is it a time sink?

### Takeaway
For a beginner on integrated graphics who wants fast, cheap, professional-looking 3D-style clips, raw GPU rental and hardware purchase are time sinks that save at most a few dollars a month; the only "rent the compute" option that competes with hosted generators on effort is the official Comfy Cloud at $20–$35 a month, and per-clip APIs for open models ($0.05–$0.30 per 5 seconds) are the cheapest way to use those models at low volume. The route genuinely wins for high-volume or control-hungry creators: custom LoRAs for a consistent character or style, 100+ generations a month, uncensored or pipeline-style workflows, or people who already know ComfyUI or Blender.

### Cited Findings
- Cheapest verified ways to run an open model per 5-second clip: Replicate's optimised Wan 2.2 at $0.05–$0.11 (2025 launch pricing); RunPod's Wan 2.2 endpoint at $0.30. [S; P] — [replicate.com/blog/wan-22](https://replicate.com/blog/wan-22); [RunPod docs: public endpoints](https://github.com/runpod/docs/blob/main/public-endpoints/reference.mdx)
- Managed, zero-set-up compute: Comfy Cloud at $20/month for 4,200 credits, GPU billed at 0.266 credits per second only while running; LoRA and model import from $35/month. [S; P] — [comfy.org/cloud/pricing](https://www.comfy.org/cloud/pricing); [Comfy docs: Comfy Cloud](https://github.com/Comfy-Org/docs/blob/main/get_started/cloud.mdx); [Comfy docs: import models](https://github.com/Comfy-Org/docs/blob/main/cloud/import-models.mdx)
- Raw rental carries fixed and hidden costs: $0.07–$0.20 per GB per month for stored models, up to 30 minutes of first start-up, templates without models, a $10 minimum top-up, and no spot discount any more. [P] — [RunPod docs: pricing](https://github.com/runpod/docs/blob/main/pods/pricing.mdx); [RunPod docs: ComfyUI tutorial](https://github.com/runpod/docs/blob/main/tutorials/pods/comfyui.mdx)
- The best open model (MiniMax H3) and HunyuanVideo 1.5 are licence-restricted in the EU and UK for local use; H3's local outputs need a paid commercial licence. [P; S] — [HunyuanVideo-1.5 LICENSE](https://github.com/Tencent-Hunyuan/HunyuanVideo-1.5/blob/main/LICENSE); [Comfy docs: MiniMax H3](https://github.com/Comfy-Org/docs/blob/main/tutorials/video/minimax/minimax-h3.mdx); [mer.vin](https://mer.vin/news/minimax-h3-open-weight-video-model-blocked-us-eu-uk/)
- Hosted closed models reached through the same ComfyUI credit system cost $0.50–$1.43 per 5-second clip (Wan 2.7 and Wan 3.0 at 720p–1080p), so open models on rented compute are several times cheaper per attempt when volume is high. [P] — [Comfy docs: partner node pricing](https://github.com/Comfy-Org/docs/blob/main/tutorials/partner-nodes/pricing.mdx)

### Inferences
- Ranking for the stated profile (weak PC, speed and low cost first):
  1. Low volume (under about 20 finished clips a month): hosted services or per-clip APIs win on both money and time; rented compute cannot beat $0.05–$0.30 per attempt once storage and idle time are counted.
  2. Medium volume, wants control or a consistent custom style: Comfy Cloud Standard or Creator. Predictable $20–$35, no infrastructure, current open models pre-installed, and partner nodes for closed models when a shot needs them.
  3. High volume (100+ generations a month) and willing to learn: a rented RTX 4090/5090 with a persistent volume, at roughly $10–$30 a month all-in, is the cheapest per clip.
  4. Buying hardware: only for sustained heavy use (tens of GPU-hours a month for a year or more) or for people who also game or do 3D work locally.
  5. Blender or Unreal on render farms or cloud PCs: only for creators who already have 3D skills; it is the slowest path to a social clip.
- Hidden costs that most "it's free and open-source" guides omit: storage rent, idle billing, 18–61 GB downloads per model, gated downloads, plan-gated LoRA import, monthly credit expiry, licence territory limits, and rising GPU prices.
- Quality caveat: open models now reach the leading closed tier only via MiniMax H3 at 768p; with the EU/UK licence problem, an EU creator relying on open weights is realistically choosing between Wan 2.2 (2025-era quality, huge LoRA ecosystem) and LTX-2.5 (fast, audio, 4K, but ranked below H3).

### Gaps
- The comparison against hosted generators uses only ComfyUI partner-node prices as a baseline; subscription pricing of hosted services is covered by other researchers and was not examined here.
- Because render farms, cloud PCs, hardware prices and beginner experience reports could not be researched, items 4 and 5 of the ranking rest on inference and should be re-checked once web access is available.
