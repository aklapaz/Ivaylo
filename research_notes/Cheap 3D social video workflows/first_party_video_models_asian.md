# First-party AI video generators from China- and Asia-based vendors: Kling, Seedance, Hailuo, Wan, Vidu, PixVerse, Hunyuan (state as of 17 November 2026)

> **Research conditions — read before using these notes.**
> - Everything below comes from 24 web-search queries run on 17 Nov 2026. The search tool returns summaries of the pages it found; I could **not open any page directly**. Direct fetches of the vendor sites (dreamina.capcut.com, klingai.com, hailuoai.video, www.vidu.com, app.pixverse.ai, wan.video) were blocked by this session's network allow-list, and the session's shared web-search budget ran out after the fourth batch of queries. So no figure here was read by me on a live vendor page; "official page" below means "the search tool reported this from that official URL".
> - Where a search summary did not say which of its listed pages a figure came from, I cite the most likely page(s) and mark it **(attribution approximate)**.
> - Because the budget ran out, several key questions (independent 3D-style reviews, free-tier details, licence/ToS terms, lawsuits, EU/UK access, generation times, SkyReels and other newcomers, Jimeng/Doubao/CapCut/BytePlus specifics) are **largely unanswered**. They are listed under Gaps, sometimes with a clearly labelled *unverified background lead* (my own pre-mid-2026 knowledge, no source retrieved) so the next pass knows what to check. Do not treat those leads as findings.
> - Many third-party pricing blogs in the results look like SEO or auto-generated pages and contradict each other. Vendor URLs are preferred; third-party figures are labelled.
> - Assumption used for "one finished 30-second video" throughout: **4 shots x 3 generations per usable shot = 12 generations of about 7.5 s each = 90 generated seconds** (for models that only offer fixed 6 s/10 s clips: 12 x 10 s clips, trimmed). Failed generations are assumed to cost full credits; editing, upscaling, music and voice-over are not included.

## 1. Current flagship model, modes and technical limits for each vendor

### Takeaway
Almost every vendor replaced its flagship in the second half of 2026: Kling 4.0 (15 Oct), Seedance 2.5 (31 Jul), MiniMax H3 / "Hailuo 3.0" (31 Jul), Wan 3.0 (beta 6 Aug, general availability late Aug), Vidu Q4 Preview (7 Oct); PixVerse's current flagship is V6 (30 Mar), and no 2026 Hunyuan Video release was found. The common spec is now 15-30 s clips with native audio, many reference inputs and 1080p-4K output, all generated in the cloud (so a PC without a GPU is not a constraint).

### Cited Findings

#### Kling AI (Kuaishou)
- Kling 4.0 is the current flagship; Kuaishou launched it on 15 Oct 2026 — [Bernama press report](https://www.bernama.com/tv/news.php?id=2622573); [nocode.mba release tracker](https://www.nocode.mba/ai-release-tracker/releases/kling-4-0)
- Kling's own feature page is titled "Kling 4.0: 30s AI Videos & Cinematic Motion", and Kling 4.0 supports clips of 3 to 30 seconds per generation — [Kling 4.0 feature page](https://kling.ai/feature/kling-4-ai-video-generation); [Kling API pricing page](https://kling.ai/dev/pricing)
- Reported Kling 4.0 specs: native 3-30 s single clips (Kling 3.0 topped out at 15 s), longer takes and multi-shot sequences, up to 10 flexible keyframes, up to 15 combined multimodal reference assets ("Omni Reference"), output up to 4K, two-channel stereo audio — [fal explainer](https://fal.ai/learn/tools/what-is-kling-4-0); [cellcog](https://cellcog.ai/blog/kling-4-0/); [Monolith Design](https://monolithdesign.agency/insights/kling-4-0-features-specs-flash); [nocode.mba tracker](https://www.nocode.mba/ai-release-tracker/releases/kling-4-0)
- 10-bit HDR at 1080p/4K is listed as a 4.0 feature by the tracker but marked "coming soon" in at least one other source (conflict) — [nocode.mba tracker](https://www.nocode.mba/ai-release-tracker/releases/kling-4-0); [Atlas Cloud spec comparison](https://www.atlascloud.ai/blog/tips/kling-4-flash-vs-full) (attribution approximate)
- 4K is not new in 4.0: Kling added native 4K output on 23 Apr 2026, and both 3.0 and 4.0 support 4K — [fal explainer](https://fal.ai/learn/tools/what-is-kling-4-0); [Wikipedia: Kling AI](https://en.wikipedia.org/wiki/Kling_AI) (attribution approximate); see also [CineD on Kling 3.0 native 4K](https://www.cined.com/kling-3-0-ai-video-model-introduced-native-4k-)
- "Kling 4.0 Flash" opened as an early-access preview on 28 Sep 2026 for top-tier annual subscribers; Flash is limited to 3-20 s at 720p, 8-bit SDR; the tracker lists it as generally available from 15 Oct — [Atlas Cloud: Kling 4.0 vs Flash](https://www.atlascloud.ai/blog/tips/kling-4-flash-vs-full); [nocode.mba tracker](https://www.nocode.mba/ai-release-tracker/releases/kling-4-0)
- Kling 3.0 (February 2026) brought consistency upgrades, more photorealistic output, clips up to 15 s and native audio generation — [TechNode Global](https://technode.global/?p=116561); [The Decoder](https://the-decoder.com/chinese-ai-video-model-kling-3-0-takes-another-step-toward-usable-creative-assets/)
- A March 2026 item describes Kling 3.0 with 2K/4K output, multimodal video and facial motion control; another page dates a Kling 3 "global launch" to 25 Mar 2026 — [AlternativeTo, Mar 2026](https://alternativeto.net/news/2026/3/kling-3-0-brings-enhanced-realism-2k-4k-output-multimodal-video-and-facial-motion-control); [cinevva](https://app.cinevva.com/news/2026-03-25-kling-3-global-launch)
- Kling maintains separate text-to-video and image-to-video product pages — [Kling AI video generator](https://kling.ai/feature/ai-video-generator); [Kling image to video](https://kling.ai/feature/image-to-video)

#### Seedance (ByteDance) on Dreamina
- Seedance 2.5 is the newest Seedance model; it launched on Dreamina on 31 Jul 2026. ByteDance announced it on Dreamina "and its ecosystem platforms" at the end of July, with API access still in preview at that point — [Dreamina launch page](https://dreamina.capcut.com/resource/seedance-2-5-launch); [knightli, 1 Aug 2026](https://knightli.com/en/2026/08/01/jimeng-seedance-2-5-global-launch-video-generation-guide/); [fal explainer](https://fal.ai/learn/tools/what-is-seedance-2-5)
- Duration: clips up to 30 s on Dreamina; on fal's API any whole second from 4 to 30 — [Dreamina launch page](https://dreamina.capcut.com/resource/seedance-2-5-launch); [fal Seedance 2.5](https://fal.ai/seedance-2.5)
- Audio: native, synchronized joint audio-video generation — [Dreamina Seedance 2.5 page](https://dreamina.capcut.com/seedance/seedance-2-5?amp=&amp=); [fal explainer](https://fal.ai/learn/tools/what-is-seedance-2-5)
- References: Dreamina advertises up to 50 multimodal references per clip; fal lists these as 30 images, 10 videos and 10 audio clips — [Dreamina launch page](https://dreamina.capcut.com/resource/seedance-2-5-launch); [fal Seedance 2.5](https://fal.ai/seedance-2.5)
- Resolution is disputed: Dreamina markets "4K & 30s", but independent testers measured 720p output on Dreamina at launch, one reviewer notes the official Seed launch article states no native resolution, and fal offers 480p/720p/1080p (720p default) — [Dreamina Seedance 2.5 page](https://dreamina.capcut.com/seedance/seedance-2-5?amp=&amp=); [DomoAI comparison](https://www.domoai.app/blog/seedance-2-5-vs-2-0); [Airmore review](https://airmore.ai/ai-review/seedance-25-review) (attribution approximate); [fal Seedance 2.5](https://fal.ai/seedance-2.5)
- A benchmark page lists "Dreamina Seedance 2.5 720p" at arena rank 6 and gives a 9 Sep 2026 announcement date, which conflicts with the 31 Jul launch date above — [gradually.ai](https://www.gradually.ai/en/ai-models/dreamina-seedance-2.5-720p/)
- Dreamina's price page lists Seedance 2.5 plus cheaper "Pro", "Fast" and "Mini" tiers; a reseller sells "Seedance 2.0 Mini & Fast" APIs — [Dreamina pricing page](https://dreamina.capcut.com/seedance/seedance-2-5-pricing-2026); [Atlas Cloud](https://www.atlascloud.ai/blog/tips/seedance-2.5-pricing-guide)
- Dreamina's Seedance hub covers text-to-video, image-to-video and AI effects; Dreamina also has a "rough cut" canvas to assemble AI clips and a Seedaudio 1.5 audio model — [Seedance hub](https://dreamina.capcut.com/seedance); [rough cut editor](https://dreamina.capcut.com/ai-video/rough-cut-video); [Seedaudio 1.5](https://dreamina.capcut.com/ai-model/seedaudio-1-5)

#### Hailuo (MiniMax)
- MiniMax H3, also called Hailuo 3.0, launched 31 Jul 2026 (one tracker dates it 30 Jul). It is described as a general-purpose omni-modal model (text, images, video and audio in one transformer) that succeeds Hailuo 2.3 — [Hailuo H3 page](https://hailuoai.video/tools/minimax-h3); [Hugging Face community post](https://huggingface.co/blog/ResterChed/minimax-h3-hailuo-3-0); [usagepricing tracker](https://usagepricing.com/blueprint/activity/minimax-2026-07-30-launch)
- Reported H3 specs: up to 2K, 24 fps, clips of 5-15 s (one source says 4 s minimum), stereo audio generated with the picture (dialogue, sound effects, ambience) — [Morphic spec sheet](https://morphic.com/resources/models/minimax-h3); [vidmuse](https://vidmuse.ai/blog/hailuo-3-0)
- H3 modes: text-to-video, image-to-video with first- and last-frame control, reference generation (up to 9 images, 3 video clips, 3 audio files, 12 files in total), plain-language editing of existing video, voice transfer — [Morphic spec sheet](https://morphic.com/resources/models/minimax-h3); [Hailuo H3 page](https://hailuoai.video/tools/minimax-h3)
- Conflict: one source says default output is 768p on the short side with 2K coming from a second step; others describe 2K as native — [vidmuse](https://vidmuse.ai/blog/hailuo-3-0); [Morphic spec sheet](https://morphic.com/resources/models/minimax-h3) (attribution approximate)
- One third-party source claims H3 placed first for video editing on the Artificial Analysis leaderboard; no independent confirmation found — [picassoia blog](https://blog.picassoia.com/hailuo-3-0-release-date-minimax-new-video-model-explained) (attribution approximate)
- Open weights are claimed or promised ("open-weight" in one post, "will be released" in another); whether they are public was not confirmed — [Hugging Face community post](https://huggingface.co/blog/ResterChed/minimax-h3-hailuo-3-0)
- The Hailuo subscribe page headline is "MiniMax H3 LIVE NOW. Top-Tier Quality, Versatile References" — [Hailuo subscribe page](https://hailuoai.video/subscribe)
- Hailuo 2.3 is still offered (768p at 6 s or 10 s, 1080p at 6 s) and is labelled legacy by a developer guide — [Hailuo 2.3 model page](https://hailuoai.video/tools/hailuo-2-3-model); [developersdigest](https://www.developersdigest.tech/models/video-generation/minimax)
- MiniMax also released H3-Image (4K image generation) — [MiniMax blog](https://www.minimax.io/blog/minimax-h3-image)

#### Wan (Alibaba)
- Wan 3.0 entered public beta on 6 Aug 2026 and reached general availability in late August on Alibaba Cloud Model Studio and Qwen Cloud, with wider wan.video access rolling out to members — [DataNorth](https://datanorth.ai/news/alibaba-launches-wan3-0-video-model); [OrcaRouter](https://www.orcarouter.ai/blog/wan-3-0-release-date); [ProPakistani, 24 Aug 2026](https://propakistani.pk/2026/08/24/alibaba-launches-wan-3-0-ai-video-model-after-raising-10-billion/)
- Wan 3.0 generates clips up to 30 s at 480p, 720p or 1080p with audio, "from any input" including documents; Alibaba itself says audio quality and on-screen text accuracy still need work — [Alibaba Cloud community blog](https://www.alibabacloud.com/blog/wan3-0-30-second-ai-video-generation-from-any-input_603452); [eWeek](https://eweek.com/news/alibaba-wan3-ai-video-documents-apac-china/)
- Wan 3.0 is API/hosted only with no downloadable weights; Alibaba's last open-weight video model is Wan 2.2 (Apache 2.0); Wan 2.7 and 2.6 remain available — [DataNorth](https://datanorth.ai/news/alibaba-launches-wan3-0-video-model); [OpenRouter listing](https://openrouter.ai/alibaba/wan-3.0); [apiyi Wan 2.7/2.6 note, May 2026](https://docs.apiyi.com/en/live/2026-05/wan-2-7-2-6-launch)
- Two API variants exist: wan3.0-video and a higher-priced wan3.0-video-prime — [Model Studio: wan3.0-video-prime](https://www.alibabacloud.com/help/en/model-studio/wan3-0-video-prime); [Alibaba Cloud blog: Wan3.0 vs Prime](https://www.alibabacloud.com/blog/603618)
- The consumer app's paid perks include up to 8 concurrent videos, 1080p output and 10-30 second videos; free accounts submit 1 video at a time — [create.wan.video pricing](https://create.wan.video/pricing)

#### Vidu (Shengshu Technology)
- Vidu Q4 Preview launched 7 Oct 2026 as a public preview; Vidu Q3 is the previous flagship; user feedback is to shape the final release and no full-release date is given — [GlobeNewswire, 7 Oct 2026](https://www.globenewswire.com/news-release/2026/10/07/3376813/0/en/shengshu-technology-launches-vidu-q4-preview-a-next-generation-ai-video-model-built-for-lifelike-performances.html); [PR Newswire](https://www.prnewswire.com/news-releases/vidu-launches-q4-preview-making-flagship-ai-video-creation-accessible-to-everyone-302901266.html)
- Q4 Preview specs: output at 540p, 720p, 1080p, 2K and 4K with 10-bit colour; up to 16 s per generation; up to 15 reference images and 3 audio clips; image-to-video and reference-to-video only (no text-only prompts in the preview) — [Pandaily](https://pandaily.com/shengshu-vidu-q4-preview-4k-video-model-reference-audio-0-09-yuan-per-second); [tech360](https://www.tech360.tv/shengshu-launches-vidu-q4-preview-with-4k-output-and-low-entry-price); [CometAPI](https://www.cometapi.com/vidu-q4-preview-launches/)
- Vendor positioning for Q4: lifelike character performance, camera work and visual effects — [GlobeNewswire, 7 Oct 2026](https://www.globenewswire.com/news-release/2026/10/07/3376813/0/en/shengshu-technology-launches-vidu-q4-preview-a-next-generation-ai-video-model-built-for-lifelike-performances.html)
- A newsletter reports Q4 Preview "debuts at No. 3 for AI video" (leaderboard not named in the search summary) — [AlphaSignal](https://alphasignal.ai/news/shengshu-s-vidu-q4-preview-debuts-at-no-3-for-ai-video)
- In the consumer app, Vidu Q3 reference-to-video comes in Flash (1080p, 1-16 s) and Cinematic (1080p, 1-16 s) — [Vidu subscription page](https://www.vidu.com/subscription/personal)
- The API lineup includes viduq3, viduq3-turbo and viduq3-mix (described by a reseller as the highest-consistency reference model), with an off-peak price column (off-peak not supported for viduq3-mix) — [Vidu API pricing docs](https://platform.vidu.com/docs/overview/pricing); [Atlas Cloud: Shengshu](https://www.atlascloud.ai/providers/shengshu)
- A single unverified mention says a "Vidu S1" was unveiled on 3 Jul 2026 — [tooljunction](https://www.tooljunction.io/ai-tools/vidu) (attribution approximate)

#### PixVerse
- PixVerse V6 was released 30 Mar 2026 with native audio synthesis, 20+ cinematic camera controls and multi-shot storytelling — [fast.io review](https://fast.io/resources/pixverse-ai-review-2026/); [PixVerse V6 docs](https://docs.pixverse.ai/PixVerse-V6-Model-Introduction-Scenarios-3343e99bf35080f9bf57c55577a7d0de)
- PixVerse C1 (April 2026) is a separate model aimed at film and TV production — [PixVerse C1 docs](https://docs.pixverse.ai/PixVerse-C1-Model-Introduction-Scenarios-33b3e99bf35080628d2cda92d29771a6)
- The API reference lists v3.5, v4, v4.5, v5, v5.5, v5.6, v6 and c1 as model values (no v7 seen) — [PixVerse platform docs: V6](https://docs.platform.pixverse.ai/v6-2056814m0) (attribution approximate)
- V6 is priced at 360p, 540p, 720p and 1080p with audio on or off, and has a "Fusion" reference mode that also accepts video references — [PixVerse API pricing](https://docs.platform.pixverse.ai/pixverse-api-pricing-2394995m0)
- PixVerse also resells other vendors' models inside its app: Sora 2 / Sora 2 Pro, and Seedance 2.0 for Pro, Premium and Ultra members — [PixVerse blog: Sora 2](https://pixverse.ai/en/blog/sora-2-now-available-on-pixverse/); [PixVerse info page](https://pixverse.ai/en/ai-info-page)

#### Tencent Hunyuan Video (hosted)
- No official Tencent announcement of a new Hunyuan Video version in 2026 was found; all results were third-party review or aggregator pages — [aitexttools review](https://aitexttools.net/tools/hunyuan-video); [theskillshift](https://theskillshift.com/ai-tools/hunyuan-video/)
- Tencent's own web platform is aimed at Chinese users; one source says the official site requires +86 phone verification, while third-party clouds (fal.ai, Replicate, Segmind) give worldwide access to the open model — [aitexttools review](https://aitexttools.net/tools/hunyuan-video); [theskillshift](https://theskillshift.com/ai-tools/hunyuan-video/) (attribution approximate)
- The model is open-weight and free to self-host — [thetoolsverse](https://thetoolsverse.com/tools/hunyuan-video-tencent-ai-generator); [superwebtricks](https://www.superwebtricks.com/tencent-hunyuan-video/)

#### Spec comparison (built only from the bullets above)

| Vendor / app | Flagship (release) | Max clip | Max resolution (claimed) | Native audio | Reference inputs | Notes |
|---|---|---|---|---|---|---|
| Kling AI | Kling 4.0 (15 Oct 2026) | 30 s (Flash: 20 s) | 4K (Flash: 720p) | Yes, stereo | 15 assets, 10 keyframes | Multi-shot; Kling 3.0 (15 s) still sold |
| Dreamina / Seedance | Seedance 2.5 (31 Jul 2026) | 30 s | "4K" marketed; 720p measured on Dreamina at launch | Yes, joint | Up to 50 (30 img / 10 video / 10 audio) | Cheaper Pro / Fast / Mini tiers |
| Hailuo / MiniMax | H3 = Hailuo 3.0 (31 Jul 2026) | 15 s | 2K (native vs upscaled disputed) | Yes, stereo | 9 img + 3 video + 3 audio (12 max) | First/last frame, text-driven edit, voice transfer; Hailuo 2.3 still sold |
| Wan (Alibaba) | Wan 3.0 (beta 6 Aug, GA late Aug 2026) | 30 s | 1080p | Yes (vendor admits weaknesses) | "Any input", incl. documents | Closed weights; Prime variant |
| Vidu | Q4 Preview (7 Oct 2026) | 16 s | 4K 10-bit | Audio references accepted (3 clips) | 15 images + 3 audio | Preview has no text-to-video; Q3 Flash / Cinematic still sold |
| PixVerse | V6 (30 Mar 2026) | not retrieved | 1080p | Yes (on/off toggle) | Fusion mode (image and video refs) | C1 film model; resells Sora 2, Seedance 2.0 |
| Tencent Hunyuan | No 2026 release found | not retrieved | not retrieved | not retrieved | not retrieved | China-centric hosting |

### Inferences
- All seven products are browser/cloud services, so the user's integrated-graphics PC only needs to run a browser and a light editor; the open-weight routes (Wan 2.2, Hunyuan Video, possibly H3) are not practical without a GPU.
- For X, Reels, TikTok and Shorts, 720p-1080p output is sufficient; the 2K/4K tiers (Kling 4.0 4K, Vidu Q4 4K, H3 2K) cost more credits and add little on phone screens. The cheaper 720p/1080p or "Flash/Fast/Mini" tiers are the relevant ones for this profile.
- Multi-reference input is now the main consistency mechanism across vendors (15 assets on Kling 4.0, up to 50 on Seedance 2.5, 12 on H3, 15+3 on Vidu Q4). For a recurring 3D character or product, the workflow is: make stylised stills first, then feed them as references or start frames.
- Vidu Q4 Preview not supporting text-only prompts means a Vidu user needs an image step first (or stays on Q3 for text-to-video).
- The official Kling site now appears to live at kling.ai (membership, developer and feature URLs all sit there), with klingai.com URLs still appearing for invitations.

### Gaps
- **9:16 vertical support** was not confirmed from any retrieved source for any vendor. *Unverified background lead:* through mid-2026 all of these apps offered a 9:16 aspect option; needs a quick check per current flagship (especially Vidu Q4 Preview and Wan 3.0).
- **Generation time on free vs paid queues**: no data retrieved for any vendor.
- **Mode-by-mode matrix** (extend, lip sync, motion control / performance transfer, video-to-video editing) is incomplete: only the items in the bullets above were seen. *Unverified background lead:* before mid-2026 Kling offered Elements, Motion Control, lip sync and extend; PixVerse offered effects templates, transition (first/last frame), fusion, extend and lip sync; Wan 2.6 offered reference-to-video and multi-shot.
- **PixVerse V6 maximum clip length** and **Hunyuan Video hosted specs** were not retrieved.
- **Seedance on CapCut, Jimeng, Doubao and BytePlus**: nothing retrieved beyond a third-party report of Volcano Engine API rates (about $0.21/s at 720p, $0.09/s at 480p) — [Atlas Cloud blog](https://www.atlascloud.ai/blog/seedance-2.0-pricing-full-cost-breakdown-2026). Which Seedance versions each of those surfaces exposes outside China is unknown.
- **Other vendors / newcomers** (SkyReels and others): no search could be run. *Unverified background leads to check:* SkyReels V4 from Skywork AI (Kunlun Tech) with joint audio-video generation; Alibaba's "HappyHorse" model that topped a public video arena in spring 2026; Baidu, Zhipu and SenseTime video products.
- Whether Kling 4.0 (full or Flash) is available on the Standard plan, or only on higher tiers, was not confirmed.

## 2. Quality for stylised 3D-animation looks and character/product consistency (independent evidence)

### Takeaway
I could not retrieve any independent review or side-by-side test of 3D-animation styles (Pixar-like characters, glossy product renders, isometric dioramas, clay/toy looks, 3D motion graphics): the search budget ran out before this question was reached. Only general leaderboard signals and reference-input specs were found, so any ranking of these tools for 3D looks would be unsupported.

### Cited Findings
- General-quality signals only (not 3D-specific): Vidu Q4 Preview reportedly "debuts at No. 3 for AI video" — [AlphaSignal](https://alphasignal.ai/news/shengshu-s-vidu-q4-preview-debuts-at-no-3-for-ai-video); "Dreamina Seedance 2.5 720p" is listed at arena rank 6 — [gradually.ai](https://www.gradually.ai/en/ai-models/dreamina-seedance-2.5-720p/); one third-party blog claims H3 ranks first for video editing on Artificial Analysis (unconfirmed) — [picassoia blog](https://blog.picassoia.com/hailuo-3-0-release-date-minimax-new-video-model-explained) (attribution approximate)
- The Decoder's headline on Kling 3.0 frames it as "another step toward usable creative assets" — [The Decoder](https://the-decoder.com/chinese-ai-video-model-kling-3-0-takes-another-step-toward-usable-creative-assets/)
- Consistency-relevant specs (vendor or host claims, not test results): Kling 4.0 takes up to 15 reference assets and 10 keyframes — [fal explainer](https://fal.ai/learn/tools/what-is-kling-4-0); Seedance 2.5 takes up to 50 multimodal references — [Dreamina launch page](https://dreamina.capcut.com/resource/seedance-2-5-launch); H3 takes 9 images, 3 videos and 3 audio files — [Morphic spec sheet](https://morphic.com/resources/models/minimax-h3); Vidu Q4 Preview takes 15 reference images and 3 audio clips — [Pandaily](https://pandaily.com/shengshu-vidu-q4-preview-4k-video-model-reference-audio-0-09-yuan-per-second); a reseller calls viduq3-mix Vidu's "highest-consistency reference model" — [Atlas Cloud: Shengshu](https://www.atlascloud.ai/providers/shengshu)
- Vidu publishes its own article on free AI animation tools (vendor content, not independent) — [Vidu blog](https://www.vidu.com/blog/free-ai-animation)
- PixVerse publishes its own V6 review and competitor comparisons (vendor content, not independent) — [PixVerse blog: V6 review](https://pixverse.ai/en/blog/pixverse-v6-ai-video-generator-review); [PixVerse vs Runway](https://pixverse.ai/en/blog/pixverse-vs-runway)

### Inferences
- Since no vendor can be ranked on 3D looks from evidence, the practical way to decide is a small paid test: run the same 3D-style start frame and the same reference set through the two or three cheapest options (see section 3) before committing to an annual plan.
- For glossy product renders and consistent mascots, image-to-video or reference-to-video from a finished 3D-style still is likely to be more controllable than text-to-video, because the look is fixed in the still and the video model only has to animate it. This is a workflow inference, not a tested result.
- Long single generations (30 s on Kling 4.0, Seedance 2.5, Wan 3.0) with multi-shot support could reduce cross-shot drift compared with stitching separate 5 s clips, but no test confirming this for stylised 3D content was found.

### Gaps
- No independent comparison of Pixar-like CG, product renders, isometric dioramas, clay/toy looks or 3D motion graphics across Kling 4.0, Seedance 2.5, H3, Wan 3.0, Vidu Q4/Q3 and PixVerse V6 was retrieved. This is the largest unanswered question in this file.
- No independent multi-shot character or product consistency tests were retrieved.
- *Unverified background lead (pre-mid-2026 reviewer consensus as I recall it, no source retrieved):* Kling was usually rated strongest for image-to-video motion and subject consistency; Seedance 2.0 for multi-reference control; Hailuo and Vidu for expressive stylised and anime-like animation; PixVerse for fast, effect-driven social clips; Wan for value. These impressions predate every current flagship and must be re-checked.

## 3. Pricing: consumer plans, credits per generation, and effective cost per clip

### Takeaway
Entry paid plans cluster around $9-10 per month on monthly billing (Kling Standard $8.80 renewal, Hailuo Standard from $9.99, Vidu Standard $10, PixVerse Standard $10, Wan Pro $10 or $5/month billed yearly), but what a clip costs differs by up to roughly 10x: about $0.15-0.40 per 5-second clip on Vidu Q3 Flash, Wan 3.0, Hailuo 2.3, PixVerse V6 and Kling 3.0 at 720p, versus roughly $0.40-1.00 or more on the newest flagships (Kling 4.0, H3 at 2K, Seedance 2.5). Kling restructured its upper tiers in October 2026, and Dreamina's list prices are obscured by constant first-month promotions, so several figures need a live check.

### Cited Findings

#### Kling AI
- Official membership page (as reported by the search tool): tiers are Standard, Pro, Premier and Ultra+. Standard is $6.99 for the first month, then $8.80, with 660 credits per month; Pro is $25.99 for the first month with 3,000 credits; Ultra+ is $432.99 for the first month with 57,000 credits — [Kling membership page](https://kling.ai/app/membership/membership-plan)
- A different snapshot of Kling's pages shows Premier at $64.99 first month with 8,000 credits and Ultra at $127.99 first month with 26,000 credits; per-100-credit prices run from about $1.06 (entry) down to about $0.76 (top tier) — [Kling membership page, alternate snapshot](https://kling.ai/app/membership/membership-plan?r=26)
- A third-party guide that says it read the official page on 14 Nov 2026 (PT): Premier is sold at 8,000, 18,000, 28,000 or 38,000 credits per month; Ultra+ has 57,000 credits; there is a Business tab. Premier 8,000 is $92.00 list, $64.99 first month, $80.96 thereafter. Ultra+ is $619.00 list, $432.99 first month, $544.99 thereafter. About $1.01 per 100 credits on Premier — [vidfare, Nov 2026](https://vidfare.com/guides/kling-ai-pricing/)
- A guide dated 20 Oct 2026 ("after the October 2026 change"): Premier 18K is $135 first month then $181.99; Ultra+ is $402 first month then $544.99 for 57,000 credits; Kling's credit cost guide of 28 Jul 2026 still listed Ultra at $159.99 a month for 26,000 credits. The first-month figures conflict with vidfare's — [Voyager](https://voyager.so/blog/kling-ai-pricing)
- Renewal and yearly prices from third-party guides: Standard $8.80/month, 660 credits, about $79.20 billed yearly — [magichour](https://magichour.ai/blog/kling-ai-pricing); Pro $32.56/month renewal, 3,000 credits, about $293.04 yearly; Premier $80.96/month renewal, 8,000 credits, about $728.64 yearly — [promptsrush](https://promptsrush.com/blog/kling-ai-pricing); Ultra $159.99/month renewal, 26,000 credits, about $1,429.99 yearly — [framesurfer](https://framesurfer.com/blogs/kling-ai-pricing)
- List prices before discounts: Standard $10, Pro $37 — [eesel](https://www.eesel.ai/blog/kling-ai-pricing). The plan page's per-credit figure is a first-month price and renewals run about 25% higher — [toolstandard, Oct 2026](https://toolstandard.com/pricing/kling-ai-pricing/)
- Kling 3.0 credit costs for a 5-second clip: 720p without audio 30 credits; 720p with audio 45; 1080p without audio 40; 1080p with audio 60 (70 with voice tone control) — [eesel](https://www.eesel.ai/blog/kling-ai-pricing); [Atlas Cloud](https://www.atlascloud.ai/blog/tips/kling-ai-pricing); [layer3labs](https://www.layer3labs.io/guides/kling-ai-pricing); [camclo3d](https://camclo3d.com/blog/kling-ai-pricing)
- Kling 4.0 consumer credit cost: one third-party guide says 10 credits per second at 720p and 15 at 1080p, sound included; an older pre-launch guide says "not published" — [genie-artificiel](https://www.genie-artificiel.com/en/ai-tools/kling/); [framesurfer](https://framesurfer.com/blogs/kling-ai-pricing) (attribution approximate)
- Official API pricing bills Kling 4.0 per second of total video: text-to-video without an input video is 1.0 unit per second at 720p and 1.5 units per second at 1080p — [Kling API pricing page](https://kling.ai/dev/pricing)

#### Dreamina (Seedance)
- Seedance 2.5 costs 37 credits per second on Dreamina; the "Pro", "Fast" and "Mini" tiers cost 17, 8 and 5 credits per second — [Dreamina pricing page](https://dreamina.capcut.com/seedance/seedance-2-5-pricing-2026)
- Current promotion: the eligible US Basic first month is $0.29 with 1,575 credits, which Dreamina works out as about $0.0068 per generated second of Seedance 2.5 at 720p. The credits are shared across models and the offer is not unlimited. Dreamina brands the sale "98% OFF" — [Dreamina pricing page](https://dreamina.capcut.com/seedance/seedance-2-5-pricing-2026); [Dreamina sale page](https://dreamina.capcut.com/resource/dreamina-summer-sale-2026)
- Plan credits: Basic includes 1,575 credits per monthly period, Standard 3,885. A Standard first-month offer works out at $0.0864 per second of Seedance 2.5 — [Dreamina October offer FAQ](https://dreamina.capcut.com/ai-video/dreamina-october-offer-faq-2026)
- Advanced annual: $450 for the first year (50% off), renewing at $900 per year, "Seedance 2.5 from $0.10/sec"; another snapshot shows "from $0.08/sec at 40% off". Annual plans have their own payment and credit schedules, and the 98%-off monthly offer does not extend to annual billing — [Dreamina Seedance price page](https://dreamina.capcut.com/seedance/seedance-price); [Dreamina October offer FAQ](https://dreamina.capcut.com/ai-video/dreamina-october-offer-faq-2026)
- Dreamina's own guide (dated 14 Aug 2026): Seedance 2.5 from about $0.097 per second on the annual Advanced plan; Seedance 2.0 from about $0.046 per second on the best monthly promotion or $0.055 per second on the best annual offer. Dreamina warns the guide is not a promise and to check live plan terms — [Dreamina Seedance price page](https://dreamina.capcut.com/seedance/seedance-price)
- No official API or standard-plan per-second table was found; an older reseller article says Dreamina exposes no API, and reports Volcano Engine rates of about $0.21/s at 720p and $0.09/s at 480p — [Atlas Cloud blog](https://www.atlascloud.ai/blog/seedance-2.0-pricing-full-cost-breakdown-2026)

#### Hailuo (MiniMax)
- The subscribe page advertises plans "From $9.99 /mo" — [Hailuo subscribe page](https://hailuoai.video/subscribe)
- Hailuo's subscription terms page (about 16 months old per the search tool) lists Standard $14.99/month with 1,000 credits, Pro $54.99/month with 4,500 and Master $119.99/month with 10,000; third-party guides add Ultra $124.99 with 12,000 and Max $199.99 with 20,000 — [Hailuo subscription terms](https://hailuoai.video/doc/payment-policy.html); [aireiter](https://aireiter.com/blog/hailuo-ai-pricing); [mobbi](https://mobbi.ai/blog/hailuo-ai-pricing) (attribution approximate)
- A blog post on Hailuo's own site gives lower prices: Standard $9.99, Pro $34.99, Master $79.99 per month — [Hailuo blog](https://hailuoai.video/pages/blog/paid-vs-free-ai-video-generators)
- Third-party figures for annual billing: Standard $7.99, Pro $27.99, Master $63.99 per month equivalent; one page lists a Standard promo at $7.99 — [FaceLoom](https://faceloom.com/blog/hailuo-ai-pricing-explained); [felloai](https://felloai.com/minimax-pricing/) (attribution approximate)
- Credit rules: membership credits are valid for one month and do not roll over; extra credits cost $1 per 70 credits — [Hailuo subscription terms](https://hailuoai.video/doc/payment-policy.html)
- Hailuo 2.3 credit costs: 768p 6 s = 25 credits; 768p 10 s = 50 credits; 1080p 6 s = 50 credits — [Hailuo 2.3 model page](https://hailuoai.video/tools/hailuo-2-3-model)
- H3 cost: Hailuo's own page estimates about $0.073-$0.120 per second at 2K depending on plan (labelled an estimate; actual credits vary by mode and plan) — [Hailuo H3 page](https://hailuoai.video/tools/minimax-h3)
- API: H3 moved video billing from $0.19-$0.56 per clip (Hailuo 2.3) to $0.08-$0.13 per second; Hailuo 2.3 Fast API is $0.19 for 768p 6 s, $0.32 for 768p 10 s and $0.33 for 1080p 6 s; prepaid Video Packages do not yet cover H3 — [magichour](https://magichour.ai/blog/hailuo-23-pricing); [MiniMax API pricing docs](https://platform.minimax.io/docs/guides/pricing-video)

#### Wan (Alibaba)
- create.wan.video plans: Free $0; Pro $5/month billed yearly (shown as $10 on monthly billing) with 300 credits per month plus daily check-ins; Premium $20/month billed yearly (shown as $40 monthly) with 1,200 credits per month. Listed perks: 8 concurrent videos, 1080p, 10-30 second videos, watermark-free downloads — [create.wan.video pricing](https://create.wan.video/pricing); [vidfare, Nov 2026](https://vidfare.com/guides/wan-3-0-unlimited/)
- Credit packs run from $1.50 for 30 credits to $100 for 3,900 credits — [aliteq](https://aliteq.com/is-wan-3-free); [vidfare, Nov 2026](https://vidfare.com/guides/wan-3-0-unlimited/) (attribution approximate)
- Credits per generation: one third-party source gives Wan 3.0 at 5 / 8.75 / 17.5 credits per 5 seconds at 480p / 720p / 1080p; the official pricing page itself does not state a per-video credit cost — [aliteq comparison, Nov 2026](https://aliteq.com/wan-3-vs-seedance-2-5) (attribution approximate); [create.wan.video pricing](https://create.wan.video/pricing)
- API list price on Alibaba Cloud Model Studio: about $0.05/s at 480p, $0.10/s at 720p, $0.20/s at 1080p, with a limited-time 30% discount on wan3.0-video and a costlier wan3.0-video-prime tier; a 30-second free quota exists in the Singapore region only — [Model Studio pricing](https://www.alibabacloud.com/help/en/model-studio/model-pricing); [Alibaba Cloud Wan 3.0 promotion](https://www.alibabacloud.com/en/campaign/wan3-promotion?_p_lc=1); [vidfare, Nov 2026](https://vidfare.com/guides/wan-3-0-unlimited/)
- Several look-alike sites (wan30.art, wan3.video, wan3pro.video, wan30.video, wan2-1.com) are not Alibaba's and quote different prices — [vidfare, Nov 2026](https://vidfare.com/guides/wan-3-0-unlimited/)

#### Vidu
- Plans as reported by most third-party sources: Standard $10/month (about $8/month billed yearly) with 800 credits; Premium $35/month (about $28 yearly) with 4,000 credits; Ultimate $99/month (about $79 yearly) with 8,000 credits. Other sources show different Premium and Ultimate figures ($43 for 3,500; $115 or $230 for 10,000 or 20,000), and the pricing page reportedly loads fully only after sign-in — [dupple review](https://dupple.com/reviews/vidu-ai); [aitoolsbakery](https://aitoolsbakery.com/blog/vidu-pricing/); [fluxnote](https://fluxnote.io/guides/vidu-ai-review) (attribution approximate)
- Credit validity: subscription credits last 30 days; purchased and bonus credits last 2 years — [Vidu pricing page](https://www.vidu.com/pricing)
- Consumer credit cost: Vidu Q3 reference-to-video is 3 credits per second in Flash (1080p, 1-16 s) and 6 credits per second in Cinematic (1080p, 1-16 s) — [Vidu subscription page](https://www.vidu.com/subscription/personal)
- Q4 Preview launch pricing: "from $0.014/sec" promotional (press release; final pricing may vary by plan and region); a second report gives $0.045/s at 540p up to $0.39/s at 4K, and RMB 0.09 per second in China; 30% off image-to-video and reference-to-video until 30 Nov 2026 — [PR Newswire](https://www.prnewswire.com/news-releases/vidu-launches-q4-preview-making-flagship-ai-video-creation-accessible-to-everyone-302901266.html); [Pandaily](https://pandaily.com/shengshu-vidu-q4-preview-4k-video-model-reference-audio-0-09-yuan-per-second); [tech360](https://www.tech360.tv/shengshu-launches-vidu-q4-preview-with-4k-output-and-low-entry-price)
- API (separate credit system): Q4 Preview reference-to-video is 24 credits/s at 1080p, 19 at 720p, 9 at 540p; a launch pack is 30,000 credits for $105 ($0.0035 per credit, valid 12 months); viduq3-turbo 720p is 10 credits/s standard and 5 off-peak; API credits were inflated 10x on 3 Nov 2025, so older figures are not comparable — [Vidu API pricing docs](https://platform.vidu.com/docs/overview/pricing); [Vidu API update notice](https://platform.vidu.com/docs/api-reference/updates)

#### PixVerse
- Plans as read from PixVerse's plan page on 13 Oct 2026 by a third party: Standard $10/month ($8/month billed yearly, $96/year) with 1,200 credits; Pro $30 ($24 yearly, $288/year) with 6,000 credits every 30 days plus 60 daily; Premium $60 ($48 yearly) with 15,000; Ultra $249 ($149 yearly) with 25,000. Another source gives Ultra at $199/month — [costbench](https://costbench.com/software/ai-video-generators/pixverse/); [hokai](https://hokai.io/guides/pixverse-pricing-free-plan-2026); [aivario](https://aivario.com/tools/pixverse) (attribution approximate)
- Official V6 per-second rates on the PixVerse platform: 720p is 9 credits/s with audio off and 12 with audio on; 1080p is 18 off and 23 on; V6 Fusion with video references costs twice the standard rate — [PixVerse API pricing](https://docs.platform.pixverse.ai/pixverse-api-pricing-2394995m0); [PixVerse platform docs: V6](https://docs.platform.pixverse.ai/v6-2056814m0)
- API credit conversion: $1 = 200 credits (May 2026) per one source, 225 credits per $1 in the docs' examples — [Atlas Cloud V6 review](https://www.atlascloud.ai/blog/guides/pixverse-v6-review); [PixVerse API pricing](https://docs.platform.pixverse.ai/pixverse-api-pricing-2394995m0) (attribution approximate)
- Conflicting third-party figures for the consumer app: "a typical generation costs around 35 credits"; V6 at 14 credits per second at 1080p. Plan panels advertise bonus credits on pack purchases of 10% (Standard), 30% (Pro) and 50% (Premium, Ultra) — [toolcolumn](https://www.toolcolumn.com/tools/pixverse); [PixVerse info page](https://pixverse.ai/en/ai-info-page) (attribution approximate)

#### Tencent Hunyuan Video
- No first-party international consumer plan was found. Third-party hosting is quoted at about $0.075 per second (fal.ai) or about $0.40 per 5-second video — [theskillshift](https://theskillshift.com/ai-tools/hunyuan-video/); [aitexttools review](https://aitexttools.net/tools/hunyuan-video) (attribution approximate)

### Inferences
All dollar figures in this subsection are my arithmetic from the cited prices and credit rates. "Monthly" means month-to-month billing at the renewal price; "annual" means the per-month equivalent when billed yearly.

**Cost per credit (entry plans)**
- Kling Standard: $8.80 / 660 = $0.0133 per credit monthly; $79.20 per year / 12 / 660 = $0.0100 annual. Kling Pro: $32.56 / 3,000 = $0.0109 monthly; $293.04 per year gives $0.0081.
- Hailuo Standard: $9.99 / 1,000 = $0.0100 per credit (or $0.0150 if the older $14.99 price applies; $0.0080 on the reported $7.99 annual rate).
- Wan Pro or Premium: $0.0333 per credit monthly ($10 / 300 or $40 / 1,200); $0.0167 annual.
- Vidu Standard: $10 / 800 = $0.0125 monthly; $0.0100 annual.
- PixVerse Standard: $10 / 1,200 = $0.0083 monthly; $0.0067 annual. PixVerse Pro: $0.0050 monthly; $0.0040 annual.

**Comparison table: effective cost on the cheapest paid plan (30-second video = 90 generated seconds, see assumption at top)**

| Vendor, plan basis | Model and setting | Credits per second | One 5 s clip | One 10 s clip | 30 s finished video | Confidence in inputs |
|---|---|---|---|---|---|---|
| Kling Standard ($8.80 monthly; $6.60/mo annual; 660 credits) | Kling 3.0, 720p, no audio | 6 | $0.40 (annual $0.30) | $0.80 ($0.60) | 540 credits = $7.20 ($5.40) | Medium: third-party guides agree |
| Kling Standard | Kling 3.0, 1080p, with audio | 12 | $0.80 ($0.60) | $1.60 ($1.20) | 1,080 credits: exceeds the 660 monthly allowance; on Pro $11.72 ($8.79 annual) | Medium |
| Kling Standard / Pro | Kling 4.0, 720p, audio included | 10 | $0.67 ($0.50) | $1.33 ($1.00) | 900 credits: exceeds Standard; on Pro $9.77 ($7.33 annual) | Low: one third-party rate, matches official API unit ratio |
| Kling Pro ($32.56 monthly; 3,000 credits) | Kling 4.0, 1080p, audio included | 15 | $0.81 | $1.63 | 1,350 credits = $14.65 ($10.99 annual) | Low |
| Dreamina (Advanced annual, first-year $450) | Seedance 2.5, 720p | 37 | 185 credits, about $0.49-0.50 | 370 credits, about $0.97-1.00 | 3,330 credits, about $8.70-9.00 | Medium for credits (official page); price is a promo rate and doubles at the $900 renewal |
| Dreamina (best promos) | Seedance 2.0 ("Pro" tier, see note) | 17 | 85 credits, about $0.23-0.28 | 170 credits, about $0.46-0.55 | 1,530 credits, about $4.10-5.00 | Medium-low: promo-based per-second rates |
| Dreamina Basic, US first month $0.29 | Any tier, 1,575 credits | 37 / 17 / 8 / 5 | 8 clips of Seedance 2.5 fit | 4 clips fit | One 30 s video fits on the 17-credit tier (1,530 credits) | Medium: one-time offer for eligible US accounts |
| Hailuo Standard ($9.99 monthly; 1,000 credits) | Hailuo 2.3, 768p | 25 per 6 s; 50 per 10 s | $0.25 (6 s clip) | $0.50 | 12 x 10 s = 600 credits = $5.99 | Medium: price page vs terms page conflict ($14.99 would give $0.37 / $0.75 / $8.99) |
| Hailuo (any plan) | H3, 2K, audio | about 12 (inferred) | $0.37-0.60 | $0.73-1.20 | $6.57-10.80 | Medium-low: vendor's own estimate range |
| Wan Pro ($10 monthly; $5/mo annual; 300 credits) | Wan 3.0, 720p | 1.75 | $0.29 (annual $0.15) | $0.58 ($0.29) | 157.5 credits = $5.25 ($2.63) | Low: credit rate from one third-party source |
| Wan Pro / Premium | Wan 3.0, 1080p | 3.5 | $0.58 ($0.29) | $1.17 ($0.58) | 315 credits = $10.50 ($5.25); just over Pro's 300 | Low |
| Vidu Standard ($10 monthly; $8/mo annual; 800 credits) | Q3 Flash, 1080p (reference-to-video rate) | 3 | $0.19 (annual $0.15) | $0.38 ($0.30) | 270 credits = $3.38 ($2.70) | Medium: credit rate official, plan price third-party |
| Vidu Standard | Q3 Cinematic, 1080p | 6 | $0.38 ($0.30) | $0.75 ($0.60) | 540 credits = $6.75 ($5.40) | Medium |
| Vidu API pack ($0.0035 per credit) | Q4 Preview, 720p / 1080p | 19 / 24 (API credits) | $0.33 / $0.42 | $0.67 / $0.84 | $5.99 / $7.56 | Medium-low: API route, launch discount to 30 Nov 2026 |
| PixVerse Standard ($10 monthly; $8/mo annual; 1,200 credits) | V6, 720p, audio off | 9 (if app = platform rate) | $0.38 (annual $0.30) | $0.75 ($0.60) | 810 credits = $6.75 ($5.40) | Low: app credit rate unconfirmed |
| PixVerse Standard | V6, 720p, audio on | 12 (same caveat) | $0.50 ($0.40) | $1.00 ($0.80) | 1,080 credits = $9.00 ($7.20) | Low |
| PixVerse Pro ($30 monthly; 6,000 credits) | V6, 1080p, audio on | 23 (same caveat) | $0.58 | $1.15 | 2,070 credits = $10.35 ($8.28 annual) | Low |
| Hunyuan via third-party host | Version not stated | n/a | about $0.38-0.40 | about $0.75 | about $6.75 | Low: aggregator sources |

- Note on Seedance tiers: the search summary did not say which generation the 17 / 8 / 5 credit tiers belong to. Because Dreamina separately quotes Seedance 2.0 at about $0.046-0.055 per second, which is 17/37 of its Seedance 2.5 rate, the 17-credit tier is most likely standard Seedance 2.0, with Fast (8) and Mini (5) below it. On those tiers a 5 s clip is 40 or 25 credits.
- Dreamina plan sizes implied by the quoted rates: "$0.097-0.10 per second" on a $450 first-year Advanced plan implies roughly 14,000 credits per month on Advanced (37 credits/s x $37.50 / $0.097-0.10). "98% off" for $0.29 implies a regular Basic monthly price in the low-to-high teens of dollars. If so, Seedance 2.5 on Basic at the regular monthly price would cost on the order of $0.30-0.45 per second, i.e. $1.50-2.25 per 5-second clip, the most expensive option in this file. Both numbers are inferences and need a live check.
- H3 credit rate: Hailuo's top-of-range estimate ($0.120/s) equals 12 credits/s at the $9.99-per-1,000-credits Standard rate, so about 12 credits per second at 2K is a reasonable guess; lower-resolution H3 output may be cheaper.
- Kling's October 2026 restructure appears to have removed the old Ultra tier (26,000 credits at $159.99, about $0.62 per 100 credits) in favour of Premier credit steps and Ultra+ at about $0.96-1.01 per 100 credits on renewal. If correct, heavy users lost the volume discount; a light solo creator on Standard or Pro is unaffected.
- Cheapest options for this creator on the numbers above (cost only; quality for 3D looks is untested): Vidu Standard with Q3 Flash (about $0.03-0.04 per second at 1080p), Wan 3.0 on an annual plan (about $0.03-0.06 per second, if the third-party credit rate is right), Hailuo 2.3 at 768p (about $0.04-0.05 per second), then PixVerse V6 720p and Kling 3.0 720p (about $0.08 per second). Kling 4.0, H3 at 2K and Seedance 2.5 are 2-10 times dearer per second.
- Monthly volume on entry plans under the 12-generation assumption: Kling Standard covers about one 30 s video per month with Kling 3.0 at 720p (540 of 660 credits); Vidu Standard covers about three with Q3 Flash (270 of 800 credits); PixVerse Standard about one and a half at 720p without audio; Hailuo Standard about one and a half with Hailuo 2.3; Wan Pro about two at 720p (157.5 of 300 credits). A creator posting several videos a week needs a mid tier or top-ups almost everywhere.
- Annual billing roughly halves Wan's price and cuts 20-25% elsewhere, but given monthly model churn in 2026, month-to-month billing is the safer default until a tool has proven itself for the user's style.

### Gaps
- **Dreamina regular (non-promotional) monthly and annual prices for Basic, Standard and Advanced** were not retrieved, nor Advanced's exact credit allowance, top-up prices or credit expiry.
- **Kling**: credit expiry/rollover rules, top-up pack prices, the exact annual prices after the October 2026 change, and whether the old Ultra tier still exists were not confirmed on the live page. Kling 4.0's consumer credit rate rests on one third-party guide.
- **Hailuo**: which price set is live ($9.99 / $34.99 / $79.99 versus $14.99 / $54.99 / $119.99), current annual prices, and H3 credits per second by resolution.
- **Wan**: per-generation credit costs are not on the official pricing page per the search tool; the only figure is third-party. Credit expiry unknown. Whether Pro removes the watermark and allows 1080p, or only Premium does, is unclear (see section 5).
- **Vidu**: plan prices come from third-party pages; Q4 Preview credit cost in the consumer app and text-to-video / image-to-video rates for Q3 were not retrieved; top-up prices not retrieved.
- **PixVerse**: whether the consumer app charges the same per-second credit rates as the platform table is unconfirmed; the Ultra price ($199 or $249) conflicts; top-up prices not retrieved.
- **Hunyuan**: no verified first-party price.

## 4. Free tiers

### Takeaway
Every vendor except possibly Hailuo still advertises some free allowance, but the terms are thin, watermarked and in flux: sources conflict on Kling (66 credits daily versus a monthly login allowance), PixVerse (30 versus 60 credits daily), Hailuo (daily credits versus one-time trial credits) and Vidu (40 or 80 credits monthly). None of the free tiers is described as licensed for commercial posting, and Dreamina's free allowance was not retrieved.

### Cited Findings
- Kling: new users get free credits at signup and returning users can claim a further allowance by logging in each month; amounts and validity may change. Free-tier exports generally carry a watermark — [Kling free credits page](https://kling.ai/explore/kling_ai_daily_free_credits); [Kling membership page](https://kling.ai/app/membership/membership-plan)
- Kling (third-party, conflicting): one guide says free accounts get 66 credits a day, about two 5-second clips, watermarked; another says the free tier has a watermark, no commercial rights and no guaranteed monthly credits, and that Kling's FAQ contradicts itself — [fluxnote](https://fluxnote.io/guides/kling-ai-pricing-2026); [toolstandard, Oct 2026](https://toolstandard.com/pricing/kling-ai-pricing/) (attribution approximate)
- Hailuo (conflicting): one source says the free tier has daily credits with 768p, watermarked, non-commercial output; another says the live pricing showed a Free plan with 0 monthly credits and "one-time free trial credits". Hailuo's terms say free users get basic generation and watermarked downloads — [Atlas Cloud](https://www.atlascloud.ai/blog/tips/hailuo-ai-pricing-cost); [aireiter](https://aireiter.com/blog/hailuo-ai-pricing) (attribution approximate); [Hailuo subscription terms](https://hailuoai.video/doc/payment-policy.html)
- Wan: Free plan is $0, one video at a time, with a daily check-in to earn credits; the page does not state how many credits a check-in gives — [create.wan.video pricing](https://create.wan.video/pricing); [aliteq](https://aliteq.com/is-wan-3-free)
- Vidu: new users receive trial credits on registering and daily login can earn more; one Vidu page says each user receives 40 free credits per month; a 2026 Vidu blog post describes roughly 10-16 free clips per month capped at 720p with a visible watermark — [Vidu pricing page](https://www.vidu.com/pricing); [Vidu AI video generator page](https://www.vidu.com/ai-video-generator); [Vidu blog](https://www.vidu.com/blog/free-ai-animation)
- Vidu (third-party, conflicting): free plan gives 80 credits plus unlimited off-peak generation, or 10 reference uses per month — [dupple review](https://dupple.com/reviews/vidu-ai); [aitoolsbakery](https://aitoolsbakery.com/blog/vidu-pricing/) (attribution approximate)
- PixVerse (conflicting): free accounts get 30 credits a day at 540p (down from 60) per one review; about 60 credits a day at 540p with a watermark per another; an older guide cites 90 signup credits plus 60 daily — [aivario](https://aivario.com/tools/pixverse); [hokai](https://hokai.io/guides/pixverse-pricing-free-plan-2026); [imagine.art](https://www.imagine.art/blogs/pixverse-ai-pricing) (attribution approximate)
- Alibaba's API (not the consumer app) has a 30-second free quota for Wan 3.0 in the Singapore region only — [vidfare, Nov 2026](https://vidfare.com/guides/wan-3-0-unlimited/)
- Dreamina's nearest thing to a free tier in the retrieved material is the $0.29 first-month Basic offer for eligible US accounts (1,575 credits) — [Dreamina pricing page](https://dreamina.capcut.com/seedance/seedance-2-5-pricing-2026)

### Inferences
- At 30 daily credits and 9-12 credits per second (if app rates match the platform table), PixVerse's free tier would yield at most a few seconds of V6 at 720p per day; at 540p it is probably one short clip per day. Useful for testing a style, not for production.
- Kling's free allowance, whichever version is right, covers a handful of watermarked test clips. A creator who wants to post commercially on X will need a paid tier on every platform here.
- The $0.29 Dreamina first month, if the user is eligible (it is described as a US offer), is the cheapest way found to produce one complete test video on Seedance (whether Basic output carries a watermark was not confirmed).

### Gaps
- Exact current free allowances, which model versions free users can run (for example whether Kling 4.0, Seedance 2.5, H3 or Wan 3.0 are open to free accounts), resolution caps and queue wait times were not confirmed for any vendor.
- Whether a payment card is required for any free tier was not retrieved (the Dreamina $0.29 offer necessarily requires payment details).
- Dreamina's free daily credits, if any remain, were not retrieved.

## 5. Usage rights, watermarks and provenance

### Takeaway
The retrieved material supports only a basic pattern: free output is watermarked and not positioned for commercial use, and paid tiers remove the visible watermark and list commercial use as a benefit (confirmed for Kling; reported for Hailuo, Vidu, PixVerse and Wan's paid tier). Tier-by-tier licence wording, invisible watermarks and provenance metadata were not retrieved for any vendor.

### Cited Findings
- Kling: free-tier exports generally include a watermark and watermark removal is a membership benefit; commercial use is permitted for eligible outputs under the applicable paid-service terms and is listed as a membership feature; users must hold rights to any reference images, music, logos or other third-party material they upload — [Kling membership page](https://kling.ai/app/membership/membership-plan); [Kling AI video generator page](https://kling.ai/feature/ai-video-generator) (attribution approximate)
- Hailuo: terms state free users get watermarked downloads while paid users get priority, more credits and watermark-free downloads; a third-party guide says free output is not licensed for commercial use — [Hailuo subscription terms](https://hailuoai.video/doc/payment-policy.html); [Atlas Cloud](https://www.atlascloud.ai/blog/tips/hailuo-ai-pricing-cost)
- Wan: watermark-free downloads are listed among paid perks; the search summary reads them as attached to Premium rather than Pro or Free — [create.wan.video pricing](https://create.wan.video/pricing)
- Vidu: Standard is described as the entry plan for watermark removal and commercial use; free output is capped at 720p with a visible watermark — [dupple review](https://dupple.com/reviews/vidu-ai) (attribution approximate); [Vidu blog](https://www.vidu.com/blog/free-ai-animation)
- PixVerse: free output is watermarked at 540p; the $10 Standard plan adds 720p and removes the watermark "for monetized posts" — [aivario](https://aivario.com/tools/pixverse); [hokai](https://hokai.io/guides/pixverse-pricing-free-plan-2026) (attribution approximate)
- Vidu's Q4 press release notes that "usage terms may vary by plan and region" — [PR Newswire](https://www.prnewswire.com/news-releases/vidu-launches-q4-preview-making-flagship-ai-video-creation-accessible-to-everyone-302901266.html)

### Inferences
- For this creator the working rule is: budget for a paid tier on whichever tool is chosen, because posting to X, Reels, TikTok and Shorts with a vendor watermark or without a commercial licence is the risk on every free tier here.
- On Wan, if watermark removal really is Premium-only, the cheapest clean-output plan is $20/month billed yearly ($240 up front) or $40 month-to-month, which removes Wan's price advantage at entry level even though the per-credit price is the same as Pro.

### Gaps
- Commercial-use wording per tier (free and each paid tier) was not read for Dreamina, Hailuo, Wan, Vidu, PixVerse or Hunyuan; Kling's is from a search summary only.
- Invisible watermarks and provenance metadata (C2PA or similar) were not retrieved for any vendor. *Unverified background lead:* China's AI-content labelling rules, in force since September 2025, require visible and metadata labels on AI-generated content from services operating in China; whether the international versions embed such labels needs checking.
- Whether the visible watermark is removed on the lowest paid tier of Dreamina and Wan is unconfirmed.

## 6. International access, payment and regional limits

### Takeaway
All six consumer products publish USD prices on English-language international sites, which indicates that users outside China can subscribe, and Hunyuan Video is the exception with China-centric hosting. No information on EU/EEA or UK restrictions, payment-card acceptance or internationally delayed features was retrieved, apart from signs of region-specific pricing at Dreamina and Vidu.

### Cited Findings
- Kling publishes USD membership prices and a separate developer API price list on its international site — [Kling membership page](https://kling.ai/app/membership/membership-plan); [Kling API pricing page](https://kling.ai/dev/pricing)
- Dreamina's headline offer is specific to "eligible US" accounts, and its Seedance price guide exists in at least German, Dutch, Swedish, Romanian, Spanish, Korean, Japanese, Thai, Tagalog and Traditional Chinese versions — [Dreamina pricing page](https://dreamina.capcut.com/seedance/seedance-2-5-pricing-2026); [German price guide](https://dreamina.capcut.com/de-de/seedance/seedance-price); [Dutch price guide](https://dreamina.capcut.com/nl-nl/seedance/seedance-price)
- Seedance 2.5 was described as launching "globally" on Dreamina on 31 Jul / 1 Aug 2026 — [knightli, 1 Aug 2026](https://knightli.com/en/2026/08/01/jimeng-seedance-2-5-global-launch-video-generation-guide/)
- Hailuo publishes USD subscription prices on hailuoai.video, and MiniMax runs an international API platform — [Hailuo subscribe page](https://hailuoai.video/subscribe); [MiniMax API pricing docs](https://platform.minimax.io/docs/guides/pricing-video)
- Wan's consumer app prices in US$, and the API is sold through Alibaba Cloud's international Model Studio, where the free quota is limited to the Singapore region — [create.wan.video pricing](https://create.wan.video/pricing); [vidfare, Nov 2026](https://vidfare.com/guides/wan-3-0-unlimited/)
- Vidu's Q4 launch quotes both USD and RMB pricing and states that pricing, resolutions, feature availability and usage terms may vary by plan and region — [PR Newswire](https://www.prnewswire.com/news-releases/vidu-launches-q4-preview-making-flagship-ai-video-creation-accessible-to-everyone-302901266.html); [Pandaily](https://pandaily.com/shengshu-vidu-q4-preview-4k-video-model-reference-audio-0-09-yuan-per-second)
- Hunyuan Video: the official Tencent site reportedly requires +86 phone verification, and international developers face real-name signup and Chinese-first documentation; third-party hosts are the practical route abroad — [aitexttools review](https://aitexttools.net/tools/hunyuan-video); [apirank](https://apirank.vip/providers/tencent/) (attribution approximate)
- Kling 4.0, Seedance 2.5 and Wan 3.0 are also sold through third-party API hosts (fal, Atlas Cloud, OpenRouter), which is another international access route — [fal: Kling 4.0](https://fal.ai/learn/tools/what-is-kling-4-0); [fal: Seedance 2.5](https://fal.ai/seedance-2.5); [OpenRouter: Wan 3.0](https://openrouter.ai/alibaba/wan-3.0)

### Inferences
- Localised Dreamina marketing pages in German, Dutch, Swedish and Romanian suggest Dreamina is marketed to EU countries, but a marketing page is not proof that sign-up, payment or Seedance 2.5 itself is available there.
- The "$0.29 first month" Dreamina price should not be assumed outside the US; a creator elsewhere should expect a different promotional or regular price at checkout.
- Hunyuan Video's first-party hosting is not a realistic option for a creator outside China; it only matters through third-party hosts, which are outside this file's scope.

### Gaps
- Not retrieved for any vendor: whether a normal international credit or debit card is accepted, which payment processors are used, VAT handling, and any EU/EEA or UK feature blocks.
- Not retrieved: which features or model versions are China-first (for example on Jimeng, Doubao, Kling's Chinese app or Hailuo's Chinese app) and how long international releases lag.
- *Unverified background lead:* Seedance 2.0's international rollout in spring 2026 was staggered by country after the copyright dispute described in section 7, with some markets served later than others. Whether Seedance 2.5 has similar country gaps (including the EU, UK and US) must be checked on Dreamina's availability pages.

## 7. Restrictions and risk: moderation, IP disputes, lawsuits, data and terms

### Takeaway
Nothing on moderation rules, studio complaints, lawsuits or data/licence terms could be researched before the search budget ran out, so this section has almost no sourced findings. The two known legal flashpoints, Hollywood's objections to Seedance 2.0 and the studios' suit against MiniMax, are recorded only as unverified leads and their 2026 status is unknown.

### Cited Findings
- Kling tells users they must hold rights to reference images, music, logos and other third-party material they upload, and ties commercial use to the paid-service terms — [Kling membership page](https://kling.ai/app/membership/membership-plan) (attribution approximate)
- Vidu's press material says usage terms may vary by plan and region — [PR Newswire](https://www.prnewswire.com/news-releases/vidu-launches-q4-preview-making-flagship-ai-video-creation-accessible-to-everyone-302901266.html)
- A third-party Vidu guide's title flags "references, credits and consent" as topics a user must handle — [troiana guide](https://troiana.net/guides/vidu/)

### Inferences
- With up to 15-50 reference uploads per generation now standard, the creator's own uploads (faces, logos, product shots, music) are the main rights exposure: the vendors' terms, as far as seen, put that responsibility on the user.
- Stylised original 3D characters and the creator's own products carry far less moderation and IP risk than real people, brand mascots or film characters, which is where filters and disputes have concentrated.

### Gaps
- **Seedance and the studios.** *Unverified background lead (my pre-mid-2026 knowledge, no source retrieved):* after Seedance 2.0 launched in February 2026, the Motion Picture Association publicly objected and Disney sent ByteDance a cease-and-desist letter over generated clips using studio characters and actor likenesses; ByteDance said it would strengthen safeguards and restricted real-person reference uploads. Whether this led to a lawsuit, what filters apply to Seedance 2.5 today, and whether they block legitimate stylised characters all need verification in Reuters, The Verge, Bloomberg or SCMP coverage.
- **MiniMax litigation.** *Unverified background lead:* Disney, Universal and Warner Bros. Discovery sued MiniMax over Hailuo in US federal court in California in September 2025. The status in November 2026 (dismissed, settled, ongoing, any injunction affecting Hailuo users) was not retrieved.
- No information was retrieved on lawsuits or regulatory actions involving Kuaishou (Kling), Alibaba (Wan), Shengshu (Vidu), PixVerse or Tencent (Hunyuan).
- Not retrieved for any vendor: content-moderation rules for real people, brands and copyrighted characters; the licence the vendor takes over uploads and outputs; whether user content is used for training and whether there is an opt-out; data location and privacy terms; account-ban or credit-forfeiture practices.

## 8. What changed during 2026

### Takeaway
2026 saw two rounds of flagship launches (Kling 3.0, Seedance 2.0 and PixVerse V6 in the first quarter; Seedance 2.5, MiniMax H3, Wan 3.0, Vidu Q4 Preview and Kling 4.0 between late July and mid-October), a shift toward per-second billing and 30-second native clips, and at least one significant plan restructuring (Kling, October). Prices and plan structures seen in articles older than about August 2026 should be treated as stale.

### Cited Findings
- February 2026: Kling 3.0 launched (15 s clips, native audio, consistency upgrades) — [TechNode Global](https://technode.global/?p=116561); [No Film School](https://nofilmschool.com/kling-3-0-ai-video-model)
- March 2026: Kling 3.0 coverage of 2K/4K output and facial motion control; a Kling 3 "global launch" is dated 25 Mar — [AlternativeTo, Mar 2026](https://alternativeto.net/news/2026/3/kling-3-0-brings-enhanced-realism-2k-4k-output-multimodal-video-and-facial-motion-control); [cinevva](https://app.cinevva.com/news/2026-03-25-kling-3-global-launch)
- 30 March 2026: PixVerse V6 released (native audio, camera controls, multi-shot); April 2026: PixVerse C1 — [fast.io review](https://fast.io/resources/pixverse-ai-review-2026/); [PixVerse C1 docs](https://docs.pixverse.ai/PixVerse-C1-Model-Introduction-Scenarios-33b3e99bf35080628d2cda92d29771a6)
- 23 April 2026: Kling added native 4K output — [fal explainer](https://fal.ai/learn/tools/what-is-kling-4-0) (attribution approximate)
- By May 2026: Wan 2.7 available alongside Wan 2.6 — [apiyi, May 2026](https://docs.apiyi.com/en/live/2026-05/wan-2-7-2-6-launch)
- 31 July 2026: Seedance 2.5 launched on Dreamina (30 s, native audio, up to 50 references), succeeding Seedance 2.0 — [Dreamina launch page](https://dreamina.capcut.com/resource/seedance-2-5-launch); [Dreamina 2.5 vs 2.0](https://dreamina.capcut.com/seedance/seedance-2-5-vs-seedance-2-0)
- 31 July 2026: MiniMax H3 replaced Hailuo 2.3 as MiniMax's video flagship and moved API billing from per clip to per second — [magichour](https://magichour.ai/blog/hailuo-23-pricing); [Hailuo H3 page](https://hailuoai.video/tools/minimax-h3)
- 6 August 2026: Wan 3.0 public beta; late August general availability; hosted-only, with Wan 2.2 remaining the last open-weight Wan model — [DataNorth](https://datanorth.ai/news/alibaba-launches-wan3-0-video-model); [ProPakistani, 24 Aug 2026](https://propakistani.pk/2026/08/24/alibaba-launches-wan-3-0-ai-video-model-after-raising-10-billion/)
- Summer to October 2026: Dreamina ran repeated "$0.29 first month / 98% off" promotions — [Dreamina sale page](https://dreamina.capcut.com/resource/dreamina-summer-sale-2026); [Dreamina October offer FAQ](https://dreamina.capcut.com/ai-video/dreamina-october-offer-faq-2026)
- 28 September 2026: Kling 4.0 Flash early access; 15 October 2026: Kling 4.0 launch — [Atlas Cloud: Kling 4.0 vs Flash](https://www.atlascloud.ai/blog/tips/kling-4-flash-vs-full); [Bernama press report](https://www.bernama.com/tv/news.php?id=2622573)
- October 2026: Kling's plan page changed; Premier gained 8,000-38,000 credit steps and an Ultra+ tier (57,000 credits, $544.99 renewal) appeared, while the 28 Jul 2026 guide had listed Ultra at $159.99 for 26,000 credits — [Voyager](https://voyager.so/blog/kling-ai-pricing); [vidfare, Nov 2026](https://vidfare.com/guides/kling-ai-pricing/)
- 7 October 2026: Vidu Q4 Preview launched with a 30% launch discount running to 30 Nov 2026 — [GlobeNewswire, 7 Oct 2026](https://www.globenewswire.com/news-release/2026/10/07/3376813/0/en/shengshu-technology-launches-vidu-q4-preview-a-next-generation-ai-video-model-built-for-lifelike-performances.html); [tech360](https://www.tech360.tv/shengshu-launches-vidu-q4-preview-with-4k-output-and-low-entry-price)
- PixVerse's free daily allowance was reportedly cut from 60 to 30 credits during 2026 — [aivario](https://aivario.com/tools/pixverse)
- No 2026 Hunyuan Video release was found — [aitexttools review](https://aitexttools.net/tools/hunyuan-video)

### Inferences
- The release cadence (a new flagship from most vendors every five to eight months) argues against annual prepayment for a solo creator: a tool that is best value in November 2026 may be superseded or repriced by spring 2027.
- Launch windows are when prices are lowest: Vidu Q4 Preview is discounted until 30 Nov 2026, Wan 3.0's API carries a "limited-time" 30% discount, and Dreamina keeps offering near-free first months. A creator can run a low-cost comparison in the next two weeks.
- Previous flagships stay on sale at lower credit rates after each launch (Kling 3.0, Hailuo 2.3, Vidu Q3, Seedance 2.0 tiers). For short social clips these older models are where the lowest reasonable cost sits.

### Gaps
- No shutdowns or renamings were confirmed or ruled out; none was searched for specifically.
- Price changes at Hailuo, Vidu and PixVerse during 2026 could not be dated; only conflicting snapshots were found.
- Seedance 2.0's February 2026 launch and its fallout were not retrieved from any source in this session (see section 7).
- Priority checks for a follow-up pass, in order: (1) live plan tables and per-generation credit costs on kling.ai, dreamina.capcut.com, hailuoai.video, create.wan.video, vidu.com and app.pixverse.ai; (2) independent 3D-style and consistency comparisons from the last six months; (3) commercial-use and licence clauses per tier; (4) Seedance and MiniMax legal status; (5) EU/EEA and UK availability and payment; (6) SkyReels and other newcomers.
