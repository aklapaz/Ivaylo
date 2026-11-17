# Verified fact sheet: Artificial Analysis leaderboards, fal.ai and kie.ai pay-per-use prices, and Higgsfield / Krea / Magnific / Artlist plans (state as of 17 November 2026)

**Method and limits (applies to every section, read first).**
- All direct reads were made on **17 Nov 2026** by downloading the page HTML with curl and reading the visible text plus the JSON embedded in the page. Hosts read directly: artificialanalysis.ai, fal.ai, kie.ai, higgsfield.ai, www.krea.ai, www.magnific.com, artlist.io. 19 web searches were completed (of 30 allowed; one further query was rejected by the search tool), only for things that could not be read directly (complaints, reseller reliability, pages on blocked hosts).
- Tags used on every figure: **[RD]** = READ DIRECTLY on 17 Nov 2026 at the linked URL. **[SS]** = SEARCH SUMMARY (the search tool's summary of the linked page; the page itself was not opened). Where useful the source type is added: vendor page, vendor blog (marketing), competitor content, third party (often affiliate-driven, treat with caution).
- "First round" means `aggregators_and_apis.md` and section 3 of `x_workflows_and_real_world_value.md`. Each check ends in a verdict: **CONFIRMS**, **CORRECTS**, **CONTRADICTS** or **NEW** (gap filled).
- What could not be read: (1) `higgsfield.ai/pricing` is a JavaScript shell whose assets sit on assets.higgsfield.ai, a blocked host; a headless-browser attempt failed (194 blocked requests). Higgsfield plan prices below therefore come from Higgsfield's own dated blog posts and its Terms, not from the live plan table. (2) Magnific's pricing page returned HTTP 200 and was read, but its help pages (`/ai/docs/...`) returned HTTP 403. (3) help.artlist.io, docs.kie.ai, api.kie.ai, Trustpilot, Reddit and BBB are blocked hosts; anything from them is [SS]. (4) Artlist's pricing page returned HTTP 200 (the expected 403 did not occur).
- All prices are USD and exclude VAT / sales tax unless stated. Billing basis (monthly or annual) is stated next to every subscription price.
- Everything marked "my calculation" or placed under Inferences is my own arithmetic or reasoning, not a vendor statement.

---

## 1. Artificial Analysis (artificialanalysis.ai) as displayed on 17 Nov 2026: top 15 image-to-video and text-to-video, top 10 text-to-image and image-editing, and best quality per dollar for image-to-video

### Takeaway
Dreamina Seedance 2.5 leads the image-to-video board (Elo 1161) at $34.12 per minute, but MiniMax H3 (768p), HeyGen Video 1 and Pika H3 Flex sit 27-47 Elo points behind it (a 54-57% head-to-head preference for Seedance) at $2.10-$4.80 per minute, so the MiniMax H3 family gives by far the best quality per dollar for image-to-video. Kling 4.0 is not on any Artificial Analysis video board, the Veo 3.1 family now ranks 27th-29th of 35, and Gemini Omni Flash 1.2 is only 14th for image-to-video.

### Cited Findings

**Board facts and methodology (all [RD], embedded page data)**
- [RD] The image-to-video board is titled "AA-Video-I2V v2.1" and "ranks video models on animating a source image into video with audio, by Elo from pairwise human preference votes". It lists 35 models with audio; the "No Audio" variant (AA-Video-I2V-Silent v2.1) lists 40. — [AA image-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/image-to-video)
- [RD] The text-to-video board (AA-Video-T2V v2.1) lists 34 models with audio and 39 without. — [AA text-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/text-to-video)
- [RD] Banner on the image-to-video tab: "Rankings reflect the October 2026 refresh: a new prompt set and model cohort, with Elo fitted on votes cast since the refresh." — [AA image-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/image-to-video)
- [RD] Price footnote: "API Pricing reflects the cost to generate 1 minute of video on the model creator's API at the settings we benchmark (1080p where offered)". — [AA image-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/image-to-video)
- [RD] Votes come from "our validated private evaluators"; Kling 3.0 1080p (Pro) is the anchor, "fixed at 1000 as the reference point for this board's Elo scale". — [AA image-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/image-to-video)
- [RD] Two model flags exist: "Research previews are private or pre-release models not available to the general public; their results are not comparable with models deployed at scale via API. Derived models are post-trained from a listed base model." — [AA image-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/image-to-video)
- [RD] Each board also has per-category boards. Use-case categories include "Animation & Gaming", "Social Media & Creator Content", "Marketing & Advertising", "Retail & Ecommerce", "Live-Action Film"; capability categories include "Camera Control", "Spatio-Temporal Consistency", "Audio Synchronization", "Dialogue & Lip Sync", "Text Rendering". "Overall" is "all use cases and capabilities, each weighted equally". — [AA image-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/image-to-video)
- [RD] The string "Kling 4" does not occur anywhere in the image-to-video or text-to-video leaderboard pages; the only Kling entries are Kling 3.0 1080p (Pro), Kling 3.0 Omni 1080p (Pro) and, on the silent boards, Kling O1 Pro. Runway Gen-4.5 and Luma Ray 3.2 appear only on the silent boards; there is no Sora entry. — [AA image-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/image-to-video); [AA text-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/text-to-video)

**Table 1a. AA-Video-I2V v2.1 (image-to-video, with audio), top 15 of 35.** [RD] — [AA image-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/image-to-video). "$/s" is my division of the listed $/min by 60. "Derived" = post-trained from the named base model.

| Rank (plausible range) | Model | Maker | Elo (95% half-width) | Samples | Listed price | $/s | Released | Open weights |
|---|---|---|---|---|---|---|---|---|
| 1 (1-2) | Dreamina Seedance 2.5 | ByteDance Seed | 1161 (±15) | 6,611 | $34.12/min | 0.569 | 31 Jul 2026 | no |
| 2 (1-3) | Utopai X | Utopai Studios | 1151 (±14) | 7,004 | "No API available" | n/a | 30 Sep 2026 | no; derived from MiniMax H3 |
| 3 (2-4) | Dreamina Seedance 2.0 | ByteDance Seed | 1141 (±14) | 6,673 | $22.45/min | 0.374 | 18 Mar 2026 | no |
| 4 (3-6) | MiniMax H3 (768p) | MiniMax | 1134 (±14) | 6,594 | $4.80/min | 0.080 | 30 Jul 2026 | yes (Hugging Face link shown) |
| 5 (4-9) | SkyReels V4 | Skywork AI | 1125 (±15) | 5,135 | $21.00/min | 0.350 | 18 Mar 2026 | no |
| 6 (4-9) | HeyGen Video 1 | HeyGen | 1124 (±14) | 6,629 | $2.40/min | 0.040 | 13 Oct 2026 | no; derived from MiniMax H3 |
| 7 (5-11) | Hyperflow H3 | Video Rebirth | 1119 (±14) | 6,853 | $9.00/min | 0.150 | 17 Sep 2026 | yes; derived from MiniMax H3 |
| 8 (5-12) | P-Video-2-Pro | Pruna AI | 1117 (±15) | 4,399 | $5.70/min | 0.095 | 17 Sep 2026 | no; derived from MiniMax H3 |
| 9 (5-12) | MiniMax H3 Max | Fal | 1116 (±14) | 6,677 | $9.60/min | 0.160 | 26 Aug 2026 | no; derived from MiniMax H3 |
| 10 (6-12) | Pika H3 Flex | Pika Art | 1114 (±15) | 4,584 | $2.10/min | 0.035 | 29 Oct 2026 | yes; derived from MiniMax H3 (768p) |
| 11 (8-13) | Wan 3.0 | Alibaba | 1109 (±14) | 6,761 | $12.00/min | 0.200 | 19 Aug 2026 | no |
| 12 (8-13) | Agnes-Video-2.5 | Sapiens AI | 1105 (±15) | 4,265 | $2.40/min | 0.040 | 22 Aug 2026 | no; derived from LTX-2.5 |
| 13 (11-13) | HiDream-O1-Video-1.0 | HiDream | 1101 (±14) | 6,976 | $5.80/min | 0.097 | 28 Aug 2026 | no |
| 14 (14) | Gemini Omni Flash 1.2 | Google | 1085 (±15) | 5,096 | $6.26/min | 0.104 | 5 Nov 2026 | no |
| 15 (15-16) | FLUX 3 | Black Forest Labs | 1069 (±14) | 6,838 | $17.40/min | 0.290 | 23 Jul 2026 | no |

- [RD] Ranks 16-35 on the same board: 16 FLUX 3 Max (Fal, derived from FLUX 3) 1068, $8.70/min; 17 Grok Imagine Video 1.5 (listed maker "SpaceXAI") 1047, $15.00; 18 Gemini Omni Flash 1.1 1044, $9.12; 19 HappyHorse-1.1 (Alibaba-ATH) 1035, $10.80; 20 Vidu Q4 Preview 1032, $5.04; 21 HappyHorse-1.0 1022, $14.40; 22 Kling 3.0 Omni 1080p (Pro) 1004, $8.40; 23 Kling 3.0 1080p (Pro) 1000 (anchor), $10.08; 24 Grok Imagine Video 1.5 Lite 999, $8.40; 25 MAGI-2 Preview (Sand.ai) 965, "Coming soon"; 26 PixVerse V6 960, $6.90; 27 Veo 3.1 955, $24.00; 28 Veo 3.1 Fast 935, $7.20; 29 Veo 3.1 Lite 931, $4.80; 30 Vidu Q3 Pro 926, $7.20; 31 LTX-2.5 Pro 912, $10.20 (open weights); 32 LTX-2.5 Fast 912, $7.80 (open weights); 33 Vidu Q3 Turbo 901, $3.90; 34 LTX-2.3 Pro 837, $4.80 (open weights); 35 LTX-2.3 Fast 832, $3.60 (open weights). — [AA image-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/image-to-video)
- [RD] Notes attached to rows: "MiniMax H3 is available in 768p or 2K only. We run it at 768p because our benchmark standard is the highest resolution at or below 1080p"; "We benchmark HeyGen Video 1 with prompt enhancement set to ultraquality"; FLUX 3 Max was "generated using the fal API with reasoning_level: high"; Veo 3.1 models "generate up to 8 seconds, so we run [them] at 8 seconds". — [AA image-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/image-to-video)
- [RD] Silent image-to-video board (AA-Video-I2V-Silent v2.1, 40 models), top 10: Utopai X 1154; Dreamina Seedance 2.5 1128; MiniMax H3 Max 1124; Bach 1.0 Pro (Video Rebirth, $7.20/min) 1124; Hyperflow H3 1123; SkyReels V4 1119; Agnes-Video-2.5 1118; MiniMax H3 (768p) 1113; P-Video-2-Pro 1109; HeyGen Video 1 1107 (half-widths ±15-17). Lower down: Runway Gen-4.5 (720p) 35th at 898 ($7.20/min, run on only 59% of prompts because of Runway's 1,000-character prompt limit), Kling O1 Pro 36th at 867, Pika 2.5 37th at 841, Luma Ray 3.2 38th at 822 ($21.60/min). Silent-mode prices differ for some models: Kling 3.0 Pro $6.72/min, Veo 3.1 $12.00, Veo 3.1 Fast $6.00, Veo 3.1 Lite $3.00, PixVerse V6 $5.40. — [AA image-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/image-to-video)

**Table 1b. Image-to-video category boards most relevant to stylised social content (with audio; each model has only about 400-750 samples per category, so half-widths are ±42-51).** [RD] — [AA image-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/image-to-video)

| Rank | "Animation & Gaming" | Elo | "Social Media & Creator Content" | Elo |
|---|---|---|---|---|
| 1 | Dreamina Seedance 2.5 | 1176 | Dreamina Seedance 2.0 | 1201 |
| 2 | Dreamina Seedance 2.0 | 1174 | Dreamina Seedance 2.5 | 1200 |
| 3 | Utopai X | 1158 | Utopai X | 1171 |
| 4 | SkyReels V4 | 1132 | SkyReels V4 | 1170 |
| 5 | Wan 3.0 | 1126 | MiniMax H3 (768p) | 1159 |
| 6 | HiDream-O1-Video-1.0 | 1116 | MiniMax H3 Max | 1156 |
| 7 | Hyperflow H3 | 1112 | Hyperflow H3 | 1144 |
| 8 | HeyGen Video 1 | 1106 | P-Video-2-Pro | 1137 |
| 9 | MiniMax H3 (768p) | 1099 | HeyGen Video 1 | 1136 |
| 10 | MiniMax H3 Max | 1094 | Pika H3 Flex | 1136 |

- [RD] On the silent "Animation & Gaming" image-to-video board the order is Seedance 2.5 1176, Utopai X 1151, Hyperflow H3 1142, Bach 1.0 Pro 1136, MiniMax H3 Max 1115, Seedance 2.0 1110, MiniMax H3 (768p) 1104, Agnes-Video-2.5 1102 (half-widths ±50-54). — [AA image-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/image-to-video)

**Table 1c. AA-Video-T2V v2.1 (text-to-video, with audio), top 15 of 34.** [RD] — [AA text-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/text-to-video)

| Rank (plausible range) | Model | Maker | Elo (95% half-width) | Samples | Listed price | Released | Open weights |
|---|---|---|---|---|---|---|---|
| 1 (1-2) | Wan 3.0 | Alibaba | 1174 (±13) | 8,089 | $12.00/min | 19 Aug 2026 | no |
| 2 (1-3) | Utopai X | Utopai Studios | 1168 (±13) | 7,442 | "No API available" | 30 Sep 2026 | no; derived from MiniMax H3 |
| 3 (2-6) | MiniMax H3 (768p) | MiniMax | 1159 (±13) | 8,225 | $4.80/min | 30 Jul 2026 | yes |
| 4 (3-7) | Dreamina Seedance 2.5 | ByteDance Seed | 1156 (±13) | 8,214 | $34.12/min | 31 Jul 2026 | no |
| 5 (3-8) | FLUX 3 Max | Fal | 1152 (±15) | 4,526 | $8.70/min | 19 Oct 2026 | no; derived from FLUX 3 |
| 6 (3-8) | Gemini Omni Flash 1.2 | Google | 1151 (±14) | 5,634 | $6.26/min | 5 Nov 2026 | no |
| 7 (4-8) | HeyGen Video 1 | HeyGen | 1149 (±13) | 7,230 | $2.40/min | 13 Oct 2026 | no; derived from MiniMax H3 |
| 8 (5-11) | MiniMax H3 Max | Fal | 1143 (±14) | 4,549 | $9.60/min | 26 Aug 2026 | no; derived from MiniMax H3 |
| 9 (7-12) | FLUX 3 | Black Forest Labs | 1136 (±13) | 7,249 | $17.40/min | 23 Jul 2026 | no |
| 10 (8-13) | SkyReels V4 | Skywork AI | 1134 (±14) | 5,507 | $21.00/min | 18 Mar 2026 | no |
| 11 (8-13) | Dreamina Seedance 2.0 | ByteDance Seed | 1133 (±13) | 7,184 | $22.45/min | 18 Mar 2026 | no |
| 12 (9-14) | P-Video-2-Pro | Pruna AI | 1128 (±15) | 4,130 | $5.70/min | 17 Sep 2026 | no; derived from MiniMax H3 |
| 13 (10-14) | Gemini Omni Flash 1.1 | Google | 1125 (±12) | 8,550 | $9.12/min | 28 Aug 2026 | no |
| 14 (10-14) | Pika H3 Flex | Pika Art | 1124 (±14) | 5,136 | $2.10/min | 29 Oct 2026 | yes; derived from MiniMax H3 (768p) |
| 15 (15-16) | Agnes-Video-2.5 | Sapiens AI | 1063 (±13) | 5,978 | $2.40/min | 22 Aug 2026 | no; derived from LTX-2.5 |

- [RD] Ranks 16-34 on the same board: 16 Grok Imagine Video 1.5 1051; 17 HappyHorse-1.1 1046; 18 Wan2.7-260612 1035 ($9.00/min); 19 MAGI-2 Preview 1035; 20 HappyHorse-1.0 1030; 21 Kling 3.0 Omni 1080p (Pro) 1016; 22 Kling 3.0 1080p (Pro) 1000 (anchor, $10.08/min); 23 Grok Imagine Video 1.5 Lite 987; 24 PixVerse V6 979; 25 Veo 3.1 963 ($24.00/min); 26 Veo 3.1 Fast 954; 27 Veo 3.1 Lite 949; 28 LTX-2.5 Fast 939; 29 LTX-2.5 Pro 938; 30 Vidu Q3 Pro 937; 31 Vidu Q3 Turbo 905; 32 LTX-2.3 Pro 885; 33 LTX-2.3 Fast 836; 34 Boreal (Creatify) 827 ($2.69/min). — [AA text-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/text-to-video)
- [RD] Silent text-to-video board, top 6: HeyGen Video 1 1146; MiniMax H3 Max 1140; FLUX 3 Max 1138; Utopai X 1137; Wan 3.0 1136; MiniMax H3 (768p) 1123. Seedance 2.5 is 10th at 1105. — [AA text-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/text-to-video)
- [RD] In the text-to-video "Animation & Gaming" category (with audio) the order is Wan 3.0 1220, HeyGen Video 1 1214, Utopai X 1195, Gemini Omni Flash 1.2 1195, MiniMax H3 Max 1178, SkyReels V4 1170, Pika H3 Flex 1165, Seedance 2.5 1162 (half-widths ±39-47). — [AA text-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/text-to-video)

**Table 1d. AA-Image-T2I v2.1 (text-to-image), top 10 of 114.** [RD] — [AA text-to-image leaderboard](https://artificialanalysis.ai/image/leaderboard/text-to-image)

| Rank | Model | Maker | Elo (half-width) | Listed price per 1,000 images | Released |
|---|---|---|---|---|---|
| 1 | GPT Image 2.6 Sunburst (max) | OpenAI | 1261 (±14) | $210.72 | 4 Nov 2026 |
| 2 | GPT Image 2.5 Sunburst (max) | OpenAI | 1229 (±10) | $210.72 | 8 Sep 2026 |
| 3 | GPT Image 2.6 Flare (max) | OpenAI | 1227 (±12) | $210.72 | 4 Nov 2026 |
| 4 | GPT Image 2.5 Flare (max) | OpenAI | 1210 (±10) | $210.72 | 8 Sep 2026 |
| 5 | GPT Image 2 (high) | OpenAI | 1192 (±11) | $211 | 21 Apr 2026 |
| 6 | Kling Image 4.0 (preview) | KlingAI | 1180 (±13) | "Coming soon" | 17 Nov 2026 |
| 7 | Nano Banana 2.1 | Google | 1176 (±12) | $33.60 | 6 Oct 2026 |
| 8 | MAI-Image-2.6 | Microsoft AI | 1168 (±12) | $38.91 | 10 Aug 2026 |
| 9 | Grok Imagine Image 2.0 | "SpaceXAI" | 1167 (±12) | $60 | 7 Aug 2026 |
| 10 | Canva Craft | Canva | 1158 (±13) | $30 | 22 Oct 2026 |

- [RD] Other entries of interest on the text-to-image board: 11 Nano Banana 2 (Gemini 3.1 Flash Image) 1143, $67; 12 Seedream 5.5 1134, $20 (released 9 Nov 2026); 13 Muse Image (Meta) 1126, $10; 16 Nano Banana Pro (Gemini 3 Pro Image) 1119, $134; 19 FLUX 3 Image 1115, $48; 20 Nano Banana 2 Lite 1110, $33.60; 21 Seedream 5.0 Pro 1103, $90; 22 Qwen-Image-3.0-Pro 1094, $40; 29 FLUX 3 Image Klein 1041, $9 (open weights); 31 Krea 2 Large 1035, $60; 37 Ideogram 4.0 (Quality) 1026, $100; 42 FLUX.2 [max] 1021, $70; 51 FLUX.2 [pro] 1004, $30; 54 FLUX.2 [dev] exactly 1000; 79 Z-Image Turbo 937, $5 (open weights). No Midjourney entry was found. — [AA text-to-image leaderboard](https://artificialanalysis.ai/image/leaderboard/text-to-image)

**Table 1e. AA-Image-Editing v2.1, top 10 of 85.** [RD] — [AA image-editing leaderboard](https://artificialanalysis.ai/image/leaderboard/editing)

| Rank | Model | Maker | Elo (half-width) | Listed price per 1,000 images | Released |
|---|---|---|---|---|---|
| 1 | GPT Image 2.6 Sunburst (max) | OpenAI | 1211 (±13) | $210.72 | 4 Nov 2026 |
| 2 | GPT Image 2.6 Flare (max) | OpenAI | 1205 (±13) | $210.72 | 4 Nov 2026 |
| 3 | GPT Image 2.5 Sunburst (max) | OpenAI | 1202 (±11) | $210.72 | 8 Sep 2026 |
| 4 | MAI-Image-2.7-Preview | Microsoft AI | 1197 (±14) | no API | 27 Oct 2026 |
| 5 | GPT Image 2.5 Flare (max) | OpenAI | 1185 (±11) | $210.72 | 8 Sep 2026 |
| 6 | Kling Image 4.0 (preview) | KlingAI | 1183 (±14) | "Coming soon" | 17 Nov 2026 |
| 7 | Seedream 5.5 | ByteDance Seed | 1160 (±14) | $28 | 9 Nov 2026 |
| 8 | Krea 3 (Ultra) | Krea | 1154 (±13) | $100 | 15 Oct 2026 |
| 9 | Nano Banana 2.1 | Google | 1152 (±12) | $33.60 | 6 Oct 2026 |
| 10 | MAI-Image-2.6 | Microsoft AI | 1150 (±12) | $38.91 | 10 Aug 2026 |

- [RD] Other entries on the editing board: 12 GPT Image 2 (high) 1140; 13 H3-Image (MiniMax, open weights) 1135, $26.54; 15 Seedream 5.0 Pro 1132, $90; 16 Muse Image 1129, $10; 17 Nano Banana 2 1126, $67; 21 FLUX 3 Image 1119, $48; 24 Nano Banana Pro 1111, $134; 35 FLUX 3 Image Klein 1069, $9. In the "Identity-Preserving Edit" category (the closest proxy for keeping a character consistent): GPT Image 2.6 Sunburst 1232, GPT Image 2.5 Sunburst 1231, GPT Image 2.5 Flare 1225, GPT Image 2.6 Flare 1218, MAI-Image-2.7-Preview 1216, Seedream 5.5 1200, Nano Banana 2.1 1196, Krea 3 (Ultra) 1187, GPT Image 2 (high) 1181, Muse Image 1176 (half-widths ±26-36). — [AA image-editing leaderboard](https://artificialanalysis.ai/image/leaderboard/editing)

**Verdicts on first-round figures (section 3 of x_workflows_and_real_world_value.md)**
- CONFIRMS: text-to-video #1 Wan 3.0 (1174, $12.00/min), #2 Utopai X (1168, no API), #3 MiniMax H3 768p (1159, $4.80/min, open weights), #4 Seedance 2.5 (1156, $34.12/min); image-to-video #1 Seedance 2.5 (1161) and #2 Utopai X (1151); anchor Kling 3.0 1080p (Pro) = 1000 at $10.08/min ($0.168/s); the silent image-to-video top four (1154, 1128, 1124, 1124); LTX and Hyperflow H3 prices.
- CORRECTS: image-to-video #3 is Dreamina Seedance 2.0 (1141, $22.45/min), not MiniMax H3; MiniMax H3 (768p) is #4 at 1134. The "1124 / 1124 cluster" was wrong for MiniMax H3 Max, which is #9 at 1116 with audio (1124 is its silent-board score); #5 is SkyReels V4 (1125) and #6 HeyGen Video 1 (1124). Hyperflow H3 is now #7 (1119), not #5.
- CORRECTS: on text-to-video, HeyGen Video 1 is #7 at 1149 (first round: 1152, rank unknown); Grok Imagine Video 1.5 Lite is #23 at 987 (first round: "17"); the #16 entry is the full Grok Imagine Video 1.5 (1051).
- NEW: Gemini Omni Flash 1.2 is #6 on text-to-video (1151) but only #14 on image-to-video (1085), priced $6.26/min. Veo 3.1 / Fast / Lite are #27-29 on image-to-video (955 / 935 / 931). Vidu Q4 Preview is #20 (1032), PixVerse V6 #26 (960), Grok Imagine Video 1.5 #17 (1047). Kling 4.0, Sora and Midjourney are absent. Category boards for animation and social content exist (Table 1b). Image boards are led by OpenAI's GPT Image 2.6 / 2.5, with Nano Banana 2.1 the best-ranked cheap model (#7 text-to-image, #9 editing, $33.60 per 1,000).

### Inferences
- **Quality per dollar for image-to-video (my calculation from Table 1a).** The price-quality frontier (models that no cheaper model beats) is: Pika H3 Flex ($2.10/min, 1114) → HeyGen Video 1 ($2.40, 1124) → MiniMax H3 768p ($4.80, 1134) → Seedance 2.0 ($22.45, 1141) → Seedance 2.5 ($34.12, 1161). Everything else is dominated: for example Wan 3.0 ($12.00, 1109), MiniMax H3 Max ($9.60, 1116), SkyReels V4 ($21.00, 1125), Gemini Omni Flash 1.2 ($6.26, 1085) and Kling 3.0 Pro ($10.08, 1000) all cost more than MiniMax H3 and score lower.
- **How big the gaps are.** Using the standard Elo formula (expected preference = 1 / (1 + 10^(-difference/400))): Seedance 2.5 is preferred over MiniMax H3 768p about 53.9% of the time (27 points), over HeyGen Video 1 55.3% (37), over Pika H3 Flex 56.7% (47), over Gemini Omni Flash 1.2 60.8% (76), over Kling 3.0 Pro 71.6% (161) and over Veo 3.1 Lite 79.0% (230). Seedance 2.5 costs 7.1 times MiniMax H3, 14.2 times HeyGen Video 1 and 16.2 times Pika H3 Flex per minute at AA's listed prices.
- The 95% intervals overlap heavily: Seedance 2.5 (1146-1176) and MiniMax H3 768p (1120-1148) overlap by 2 points, and ranks 4-10 (1134 down to 1114) are statistically one cluster (AA's own "range" column puts MiniMax H3 at 3-6 and Pika H3 Flex at 6-12).
- For animated content specifically the premium for Seedance looks larger: in "Animation & Gaming" (image-to-video, with audio) Seedance 2.5 leads MiniMax H3 768p by 77 points (about 61% preference) and HeyGen Video 1 by 70 (about 60%). With half-widths of ±44-45 this is suggestive, not conclusive. On the silent overall board the gap nearly vanishes (Seedance 2.5 1128 vs MiniMax H3 Max 1124 and MiniMax H3 768p 1113), which matters if the creator adds music and voice in an editor anyway.
- AA's listed prices are the model maker's own API at the benchmarked setting (normally 1080p with audio), so they overstate what a 720p/768p clip costs on a marketplace: MiniMax H3 is $0.08/s on AA but $0.06/s at 768p on fal and $0.04/s on kie.ai; HeyGen Video 1 is $0.04/s on AA but $0.02/s at 768p on fal (section 2). AA's $8.70/min for FLUX 3 Max equals fal's temporary 50%-off price ($0.145/s at 1080p until 22 Nov 2026), so that entry will look twice as expensive once the promotion ends.
- Seven of the top ten image-to-video models are MiniMax H3 or post-trained derivatives of it (Utopai X, HeyGen Video 1, Hyperflow H3, P-Video-2-Pro, MiniMax H3 Max, Pika H3 Flex). Open weights do not help a user with integrated graphics directly, but they explain why near-frontier quality is available from several hosts at $0.02-$0.08 per second.
- The first round reported Gemini Omni 1.2 Flash as #1 on the separate Arena (LMArena) board for both tasks. On Artificial Analysis it is #6 for text-to-video and #14 for image-to-video, so the two arenas disagree strongly on Google's model for image-to-video; this is a reason not to treat either ranking as exact.

### Gaps
- Kling 4.0 has no Artificial Analysis rating (not listed on any video board; the Kling model-family URL returned 404). Its quality relative to the table above is unknown from this source. [SS] One third-party page claimed Kling 4.0 was still rolling out in October; this was not verified — [OrcaRouter](https://www.orcarouter.ai/ja/blog/kling-4-0-release-date).
- AA's "Compare Providers" page needs a model selection made in the browser and showed no data in the static HTML, so per-provider prices (fal vs maker API) could not be read from AA.
- The video-editing leaderboard and the full methodology text for the v2.1 video boards (prompt-set size, evaluator pool) were not read.
- Category boards rest on a few hundred samples per model; rankings inside the top ten of a category are not statistically reliable.
- Midjourney is not on the AA image boards, so no blind-vote comparison with it is available here.

---

## 2. fal.ai: image-to-video and image prices, surcharges, free credits, minimum top-up, and usability of the web playground

### Takeaway
On fal.ai a 5-second image-to-video clip costs about $0.10 (HeyGen Video 1, 768p), $0.30 (MiniMax H3, 768p), $0.40-$0.50 (MiniMax H3 Max 768p, Gemini Omni Flash 1.2 720p, Wan 3.0 720p), $0.79 (Kling 4.0 720p) and $2.31-$2.37 (Seedance 2.5 720p), with audio included on most current models and 1080p costing 1.5 to 3 times the 720p or 768p rate. A non-programmer can run every model from a form-based Playground or the Sandbox after signing in and prepaying credits; fal's own documentation states no fixed sign-up bonus and no minimum top-up.

### Cited Findings

**Table 2a. fal.ai image-to-video prices per second of output.** All [RD] from each model's page at `https://fal.ai/models/<endpoint>`; the per-model `llms.txt` files gave the same text for the five endpoints re-checked. "5 s" is my multiplication.

| Model (fal endpoint) | Price per second | Audio / resolution surcharge | 5 s clip |
|---|---|---|---|
| Seedance 2.5 ([bytedance/seedance-2.5/image-to-video](https://fal.ai/models/bytedance/seedance-2.5/image-to-video)) | about $0.2205 (480p), $0.4730 (720p), $1.164 (1080p); billed by tokens at $0.0214 per 1,000 (480p/720p) and $0.0234 (1080p) | audio included; 1080p is 2.46x the 720p rate; 4-30 s per clip | $1.10 / $2.37 / $5.82 (fal's own worked example: 5 s at 720p 16:9 = 108,000 tokens ≈ $2.31; 30 s at 720p ≈ $13.87) |
| Seedance 2.5 Flash ([.../flash/image-to-video](https://fal.ai/models/bytedance/seedance-2.5/flash/image-to-video)) | about $0.1442 (480p), $0.3094 (720p) | no 1080p listed | $0.72 / $1.55 |
| Seedance 2.0 ([bytedance/seedance-2.0/image-to-video](https://fal.ai/models/bytedance/seedance-2.0/image-to-video)) | $0.3034 (720p; the page's table says $0.3024), $0.682 (1080p) | "audio generation is included at no extra cost" | $1.51 / $3.41 |
| Seedance 2.0 Fast ([.../fast/image-to-video](https://fal.ai/models/bytedance/seedance-2.0/fast/image-to-video)) | $0.2419 (720p) | audio included | $1.21 |
| Seedance 2.0 Mini ([.../mini/image-to-video](https://fal.ai/models/bytedance/seedance-2.0/mini/image-to-video)) | about $0.0721 (480p), $0.1547 (720p) | | $0.36 / $0.77 |
| Kling 4.0 ([kling/v4/image-to-video](https://fal.ai/models/kling/v4/image-to-video)) | $0.157 (720p), $0.235 (1080p) | 3-30 s per clip; no separate audio rate shown | $0.79 / $1.18 |
| Kling 4.0 Flash ([kling/v4/flash/image-to-video](https://fal.ai/models/kling/v4/flash/image-to-video)) | $0.094 (720p) | | $0.47 |
| Kling 3.0 Pro ([fal-ai/kling-video/v3/pro/image-to-video](https://fal.ai/models/fal-ai/kling-video/v3/pro/image-to-video)) | $0.112 audio off | $0.168 audio on; $0.196 with voice control; up to 15 s | $0.56 / $0.84 / $0.98 |
| Kling 3.0 Standard ([.../v3/standard/image-to-video](https://fal.ai/models/fal-ai/kling-video/v3/standard/image-to-video)) | $0.084 audio off | $0.126 audio on; $0.154 voice control | $0.42 / $0.63 / $0.77 |
| Kling 3.0 Turbo Pro / Turbo Standard ([turbo/pro](https://fal.ai/models/fal-ai/kling-video/v3/turbo/pro/image-to-video), [turbo/standard](https://fal.ai/models/fal-ai/kling-video/v3/turbo/standard/image-to-video)) | $0.14 / $0.112 | | $0.70 / $0.56 |
| Kling O3 Standard / Pro ([o3/standard](https://fal.ai/models/fal-ai/kling-video/o3/standard/image-to-video), [o3/pro](https://fal.ai/models/fal-ai/kling-video/o3/pro/image-to-video)) | $0.084 / $0.112 audio off | $0.112 / $0.14 audio on | $0.42-$0.70 |
| Veo 3.1 ([fal-ai/veo3.1/image-to-video](https://fal.ai/models/fal-ai/veo3.1/image-to-video)) | $0.20 without audio (720p or 1080p) | $0.40 with audio; 4K $0.40 / $0.60; max 8 s per generation | $1.00 / $2.00 |
| Veo 3.1 Fast ([.../fast/image-to-video](https://fal.ai/models/fal-ai/veo3.1/fast/image-to-video)) | $0.10 without audio | $0.15 with audio; 4K $0.30 / $0.35 | $0.50 / $0.75 |
| Veo 3.1 Lite ([.../lite/image-to-video](https://fal.ai/models/fal-ai/veo3.1/lite/image-to-video)) | $0.03 (720p, no audio) | $0.05 (720p with audio); 1080p $0.05 / $0.08 | $0.15 / $0.25 |
| Gemini Omni Flash 1.2 ([google/gemini-omni-flash/v1.2/image-to-video](https://fal.ai/models/google/gemini-omni-flash/v1.2/image-to-video)) | $0.0273 (360p), $0.0819 (720p), $0.1229 (1080p), $0.2457 (4K) | "native audio is included"; plus input tokens at $1.50 per million; 3-15 s | $0.14 / $0.41 / $0.61 / $1.23 |
| Gemini Omni Flash 1.1 ([.../v1.1/image-to-video](https://fal.ai/models/google/gemini-omni-flash/v1.1/image-to-video)) | $0.03 (360p), $0.10 (720p), $0.15 (1080p), $0.30 (4K) | | $0.50 at 720p |
| MiniMax H3 ([minimax/h3/image-to-video](https://fal.ai/models/minimax/h3/image-to-video)) | $0.05 (480p), $0.06 (768p), $0.13 (2K), $0.16 (4K) | "480P and 768P are native generation modes; 2K and 4K upscale a 768P base result"; default is 2K | $0.25 / $0.30 / $0.65 / $0.80 |
| MiniMax H3 Max, fal's post-trained H3 ([minimax/h3-max/image-to-video](https://fal.ai/models/minimax/h3-max/image-to-video)) | standard rates "from November 16, 2026": $0.05 (480p), $0.08 (768p), $0.16 (1080p) | promotions ended 15 Nov (30% off: $0.035 / $0.056 / $0.112) | $0.25 / $0.40 / $0.80 |
| MiniMax H3 Max Turbo ([minimax/h3-max-turbo/image-to-video](https://fal.ai/models/minimax/h3-max-turbo/image-to-video)) | standard: $0.025 (480p), $0.04 (768p), $0.08 (1080p) | | $0.13 / $0.20 / $0.40 |
| HeyGen Video, "built on MiniMax H3 and post-trained by HeyGen" ([heygen/heygen-video/image-to-video](https://fal.ai/models/heygen/heygen-video/image-to-video)) | regular price $0.02 (480p and 768p), $0.06 (1080p and 2K) | page still shows a 50% promotion "until October 31, 2026" ($0.01 / $0.03); 5-15 s clips "with generated sound" | $0.10 / $0.30 at regular price |
| Wan 3.0 ([alibaba/wan-3.0/image-to-video](https://fal.ai/models/alibaba/wan-3.0/image-to-video)) | $0.05 (480p), $0.10 (720p), $0.20 (1080p) | "Pricing is subject to change" | $0.25 / $0.50 / $1.00 |
| Wan 3.0 Prime ([alibaba/wan-3.0-prime/image-to-video](https://fal.ai/models/alibaba/wan-3.0-prime/image-to-video)) | $0.068 / $0.14 / $0.28 | | $0.70 at 720p |
| Wan 2.7 ([fal-ai/wan/v2.7/image-to-video](https://fal.ai/models/fal-ai/wan/v2.7/image-to-video)) | $0.10 (720p), $0.15 (1080p) | | $0.50 / $0.75 |
| Vidu Q4 ([fal-ai/vidu/q4/image-to-video](https://fal.ai/models/fal-ai/vidu/q4/image-to-video)) | $0.0315 (540p), $0.0665 (720p), $0.084 (1080p), $0.133 (2K), $0.273 (4K) | | $0.16 / $0.33 / $0.42 |
| Vidu Q3 / Q3 Turbo ([q3](https://fal.ai/models/fal-ai/vidu/q3/image-to-video), [q3 turbo](https://fal.ai/models/fal-ai/vidu/q3/image-to-video/turbo)) | $0.07 / $0.035 at 360p-540p | "2.2x for 720p and 1080p" (= $0.154 / $0.077) | $0.77 / $0.39 at 720p |
| Grok Imagine Video 1.5 ([xai/grok-imagine-video/v1.5/image-to-video](https://fal.ai/models/xai/grok-imagine-video/v1.5/image-to-video)) | $0.08 (480p), $0.14 (720p), $0.25 (1080p) | each reference image adds $0.01 | $0.40 / $0.70 / $1.25 |
| FLUX 3 Max video ([blackforestlabs/flux-3-max/image-to-video](https://fal.ai/models/blackforestlabs/flux-3-max/image-to-video)) | 50% promotion to 22 Nov 2026: $0.085 (720p), $0.145 (1080p) | regular $0.17 / $0.29 "resume on November 23, 2026" | $0.43 now, $0.85 regular (720p) |
| FLUX 3 video ([blackforestlabs/flux-3/image-to-video](https://fal.ai/models/blackforestlabs/flux-3/image-to-video)) | $0.17 (720p), $0.29 (1080p), $0.32 (2K), $0.47 (4K) | | $0.85 at 720p |
| PixVerse V6 ([fal-ai/pixverse/v6/image-to-video](https://fal.ai/models/fal-ai/pixverse/v6/image-to-video)) | without / with audio: 360p $0.025 / $0.035; 540p $0.035 / $0.045; 720p $0.045 / $0.060; 1080p $0.090 / $0.115 | | $0.23 / $0.30 at 720p |
| LTX-2.5 Fast ([lightricks/ltx-2.5/image-to-video/fast](https://fal.ai/models/lightricks/ltx-2.5/image-to-video/fast)) | $0.09 (720p), $0.13 (1080p), $0.19 (1440p), $0.30 (4K) | audio included | $0.45 at 720p |
| Happy Horse 1.1 ([alibaba/happy-horse/v1.1/image-to-video](https://fal.ai/models/alibaba/happy-horse/v1.1/image-to-video)) | $0.14 (720p), $0.18 (1080p) | native audio | $0.70 at 720p |

- [RD] fal's general pricing page shows only a sample table with normalised values that differ from the model pages (for example "Kling Video v3 Image to Video [Pro] $0.14 per second" and "H3 Max Image to Video $0.03 per second"); it says the values are "based on an estimated average video = 5 seconds at 720p". The model pages state the actual billing rules. — [fal pricing](https://fal.ai/pricing)
- [RD] Every model page checked carries a "Commercial use" badge; Kling 4.0, Gemini Omni Flash 1.2, HeyGen Video and MiniMax H3 also carry a "Partner" badge. fal's FAQ: "Most models on fal are available for commercial use and are marked with a Commercial use badge on the model page. Models marked Research only are restricted to non-commercial use." — [fal FAQ](https://fal.ai/docs/documentation/model-apis/faq.md)
- [RD] Vendor marketing claim on fal's FLUX 3 Max page: it "ranks joint #1 in the preliminary Artificial Analysis image-to-video evaluation" and generates a 10-second video in about 11 seconds versus 277.8 seconds for Seedance 2.5. On the AA board read today FLUX 3 Max is #16 for image-to-video with audio (Table 1a). — [fal FLUX 3 Max](https://fal.ai/models/blackforestlabs/flux-3-max/image-to-video)

**Table 2b. fal.ai image-model prices per image.** All [RD].

| Model (page) | Price | Notes |
|---|---|---|
| Nano Banana 2.1 ([google/nano-banana-2.1](https://fal.ai/models/google/nano-banana-2.1)) | token-billed; representative cost $0.040 (1K), $0.059 (2K), $0.134 (4K) | editing with two 1K input images: $0.044 / $0.063 / $0.138; each input image is about $0.002; "no flat per-image fees or surcharges for resolution, web search, or thinking" |
| Nano Banana 2 ([fal-ai/nano-banana-2](https://fal.ai/models/fal-ai/nano-banana-2)) | $0.08 per image | 2K x1.5, 4K x2, 0.5K x0.75; web search +$0.015; high thinking +$0.002 |
| Nano Banana Pro ([fal-ai/nano-banana-pro](https://fal.ai/models/fal-ai/nano-banana-pro)) | $0.15 per image | 4K charged double; web search +$0.015 |
| Nano Banana Lite ([google/nano-banana-lite](https://fal.ai/models/google/nano-banana-lite)) | token-billed ($37.50 per million image output tokens), fixed 1K output | per-image figure not stated |
| Nano Banana, original ([fal pricing](https://fal.ai/pricing)) | $0.0398 per image | |
| Seedream 5.5 ([text-to-image](https://fal.ai/models/bytedance/seedream/v5.5/text-to-image), [edit](https://fal.ai/models/bytedance/seedream/v5.5/edit)) | $0.03 at 1K or 1.5K, $0.0405 at 2K | editing adds $0.012 per input image per output (two inputs, one output: $0.054 at 1.5K) |
| Seedream 5.0 Pro ([text-to-image](https://fal.ai/models/bytedance/seedream/v5/pro/text-to-image)) | "tentative" $0.0675 up to 1536x1536, $0.135 up to 2048x2048 | "Final pricing is not yet confirmed" |
| Seedream 5.0 Lite ([text-to-image](https://fal.ai/models/bytedance/seedream/v5/lite/text-to-image)) | $0.035 per image | |
| GPT Image 2 ([openai/gpt-image-2](https://fal.ai/models/openai/gpt-image-2)) | 1024x1024: $0.006 low, $0.053 medium, $0.211 high | 1920x1080: $0.005 / $0.040 / $0.158; default quality is high |
| GPT Image 2.5 Flare ([text-to-image](https://fal.ai/models/openai/gpt-image-2.5/flare/text-to-image)) | 1024x1024: $0.00588 low, $0.01317 medium, $0.05268 high, $0.09366 xhigh, $0.21072 max | token-billed ($30 per million image output tokens) |
| GPT Image 2.6 Flare / Sunburst ([flare](https://fal.ai/models/openai/gpt-image-2.6/flare/text-to-image), [sunburst](https://fal.ai/models/openai/gpt-image-2.6/sunburst/text-to-image)) | same token rates as 2.5 ($8 input / $30 output per million image tokens) | no per-size table on the page |
| FLUX 3 Image ([text-to-image](https://fal.ai/models/blackforestlabs/flux-3/text-to-image)) | $0.048 for a 1K (1 megapixel) image | "one flat price per image, set by resolution" |
| Krea 3 ([krea/v3/text-to-image](https://fal.ai/models/krea/v3/text-to-image)) | $0.025 per megapixel | reference images are billed too |
| Qwen Image 3 ([text-to-image](https://fal.ai/models/alibaba/qwen-image-3/text-to-image)) | $0.04 (1K), $0.075 (2K) | |
| Z-Image Turbo, FLUX.1 schnell ([fal pricing](https://fal.ai/pricing)) | $0.005 and $0.003 per megapixel | |

**Billing, free credits, minimum top-up, usability**
- [RD] "fal uses a prepaid credit model. You purchase credits in advance and they are drawn down as you use the platform." Billing is per output; "Server errors are never billed" and queue time is free, but "client-side errors like invalid inputs (HTTP 422) may still be charged". — [fal pricing docs](https://fal.ai/docs/documentation/model-apis/pricing.md); [fal FAQ](https://fal.ai/docs/documentation/model-apis/faq.md)
- [RD] "Purchased credits expire 365 days from the date of purchase. Free credits and coupons have variable expiration depending on the specific grant, ranging from 1 week to 1 year." When the balance falls below the account's lock threshold, the account is locked until credits are added. — [fal FAQ](https://fal.ai/docs/documentation/model-apis/faq.md)
- [RD] Free credits: fal's documentation names no fixed sign-up amount. It says "Sandbox occasionally offers free credits for specific models" through "global campaigns (available to all users)" and "user-specific grants", and "free credits and free request coupons are only usable in Sandbox and the Playground — they cannot be used through the API or Workflows." The MiniMax H3 Max model page shows a "Try free" label next to "Open in Sandbox". — [fal docs, full text](https://fal.ai/docs/llms-full.txt); [fal H3 Max page](https://fal.ai/models/minimax/h3-max/image-to-video)
- [SS, third party, sources disagree] New-account free credit is reported as $1 by one site and about $20 (with a business email) by others; one blog notes that fal's pricing page and documentation publish no amount. — [vantaige](https://vantaige.io/ai-tool/fal-ai); [PicassoIA blog](https://blog.picassoia.com/fal-ai-pricing-api-costs-free-credits-and-mcp)
- [RD] Minimum top-up: not stated anywhere in fal's public documentation (the purchase screen is behind login). [SS, third party] One price tracker says there are no subscriptions or minimum commitments. — [fal pricing docs](https://fal.ai/docs/documentation/model-apis/pricing.md); [CostBench](https://www.costbench.com/software/ai-media-apis/fal-ai/)
- [RD] Concurrency: "New accounts start at 2 concurrent requests. As you purchase credits, the limit increases automatically up to 40." Requests over the limit queue; they are not rejected. — [fal concurrency docs](https://fal.ai/docs/documentation/model-apis/concurrency-limits.md)
- [RD] Web playground: "Every model on fal has a Playground where you can try it with real inputs, see outputs, and copy working code"; "the Playground tab lets you fill in inputs and run the model directly in your browser." The image-to-video pages show a form with prompt, image upload ("drag and drop image files from your computer ... paste from clipboard"), end image, duration, resolution, a "Pricing details" link and a Run button; signed-out visitors see "Sign in to run". — [fal docs, full text](https://fal.ai/docs/llms-full.txt); [fal H3 Max page](https://fal.ai/models/minimax/h3-max/image-to-video)
- [RD] Sandbox: "your creative playground for testing and comparing the latest AI models ... Compare models side-by-side, estimate costs before running"; results carry "Fastest", "Cheapest" and "Free" badges. — [fal docs, full text](https://fal.ai/docs/llms-full.txt)
- [RD] fal Agent (a chat-style production assistant) is "in Early Access. Access is enabled by default for signed-in accounts." "fal bills model runs only ... Everything else in fal Agent is free to use." Optional monthly credit plans: Starter $50/month ($50 of credits, no discount), Pro $200/month (5% off UI, Sandbox, Playground and CLI usage), Max $1,000/month (10% off); credits roll over; API usage is never discounted. By default the agent asks for confirmation on video runs when the projected cost of a turn exceeds $5. — [fal Agent access and pricing](https://fal.ai/docs/documentation/agent/access-and-pricing.md); [fal Agent](https://fal.ai/agent)
- [RD] Generated files are kept "at least 7 days by default" and media URLs are public by default; fal advises downloading anything that must be kept. — [fal FAQ](https://fal.ai/docs/documentation/model-apis/faq.md)
- [SS, small sample] fal's Trustpilot pages show 2.6 from 4 reviews (Canada page), 2.9 from 11 (Belgium page) and, per a third-party review, 2.4 from 17; complaints include a $20 top-up that did not reach the balance and a $300+ balance not refunded after a suspected-fraud flag; fal replies publicly to many reviews. — [Trustpilot, fal.ai](https://ca.trustpilot.com/review/fal.ai); [aireiter review, third party](https://aireiter.com/blog/fal-ai-review-2026)

**Verdicts on first-round figures (section 7 of aggregators_and_apis.md)**
- CONFIRMS: Veo 3.1 ($0.20 / $0.40; 4K $0.40 / $0.60), Veo 3.1 Fast ($0.10 / $0.15), Veo 3.1 Lite ($0.03 / $0.05 at 720p); Kling 3.0 Pro ($0.112 / $0.168 / $0.196) and Standard ($0.084 / $0.126); Seedance 2.0 ($0.3024-$0.3034 at 720p, Fast $0.2419, 1080p $0.682); Wan 3.0 ($0.05 / $0.10 / $0.20) and Wan 2.7 ($0.15 at 1080p).
- NEW (first-round gap "fal prices for Seedance 2.5, Kling 4.0 and MiniMax H3 not retrieved"): Seedance 2.5 $0.2205 / $0.4730 / $1.164; Kling 4.0 $0.157 / $0.235 (identical to the Replicate and Runware prices in the first round, so the uniform list price is confirmed); MiniMax H3 $0.05 / $0.06 / $0.13 / $0.16.
- CORRECTS: the first round used "Seedance 2.5 720p = $1.17 per 5 s" (Runware) as "the API price". On fal the same clip costs $2.31-$2.37, about twice as much, so API prices for Seedance 2.5 are not uniform.
- NEW: image prices (first-round gap) are now given in Table 2b.

### Inferences
- A solo creator who does not code can use fal: sign in, add credits, open a model page, upload the start image, type the prompt, choose duration and resolution, press Run, download the MP4. The pages are still developer-styled (JSON results, schema tabs), there is no project library or editor, and files are deleted after about a week by default, so clips must be downloaded immediately.
- 768p is the native resolution of the MiniMax H3 family (fal says 2K and 4K are upscales of a 768p result), so paying $0.13/s for "2K" H3 buys an upscale, not more generated detail. For vertical social video a separate upscaler step is likely to be cheaper; that was not priced here.
- On most current models audio is bundled (Seedance, Gemini Omni, HeyGen, LTX, Happy Horse); a separate audio surcharge exists on Kling 3.0 (+50%), Veo 3.1 (+50% to +100%), Veo 3.1 Lite (+60-67%) and PixVerse V6 (+28-40%).
- Promotions make fal prices time-dependent: H3 Max went from $0.052 to $0.056 to $0.08 per second at 768p between late October and 16 November, and FLUX 3 Max doubles on 23 November. The HeyGen page still displays a promotion that expired on 31 October, so the price actually charged ($0.02 or $0.01 per second at 768p) should be read from the "Pricing details" control before a batch is run.
- The "Partner" badge and the fact that Artificial Analysis lists "Fal" as the maker of two ranked models suggest fal has direct relationships with model owners; this is my reading, not a statement by fal.

### Gaps
- The exact minimum credit purchase and any standard sign-up bonus on fal could not be verified (dashboard is behind login; third-party figures conflict).
- Pika H3 Flex, SkyReels V4, Hyperflow H3 and P-Video-2-Pro (all in the AA top ten) were not found on fal by its search; they may be listed under other names.
- Krea 3 and GPT Image 2.6 per-image costs on fal are only given as token or megapixel rates.
- Whether fal's Seedance 2.5 endpoints carry any regional restriction for EU users was not checked.

---

## 3. kie.ai: prices, minimum top-up, operator, and evidence on reliability and legitimacy

### Takeaway
kie.ai is a pay-as-you-go credit reseller (1 credit ≈ $0.005, smallest pack $5, credits never expire, 80 free credits) run by NEXUSAI SERVICES LLC of Denver, Colorado, and it undercuts fal by about 10% on Kling, 20-36% on Wan, MiniMax H3 and Seedance 2.5, 45-59% on Gemini Omni Flash 1.2 and about 84% on Grok Imagine Video. Its legitimacy as a business is not in doubt from what was found, but it does not say how it sources capacity at these discounts, its small Trustpilot sample is poor (about 2.1 of 5 from 16 reviews) and it has no public status page, so it is a cheap option to use with small balances rather than a platform to depend on.

### Cited Findings

**Billing and operator**
- [RD] "Pay as you go with credits (1 credit ≈ $0.005). Each model is billed per image, per second, per video or per million tokens, and failed tasks are never charged." "Credits are pay-as-you-go: there is no subscription and credits never expire. Larger top-ups include bonus credits; for example, a $1,250 top-up adds 10%." The price list holds 676 price rows for 144 models (371 video, 172 image); the embedded data was fetched at 08:00 UTC on 17 Nov 2026. — [kie.ai pricing](https://kie.ai/pricing)
- [RD] "New Kie.ai users receive 80 free credits for testing" (80 credits = $0.40). — [kie.ai Seedance 2.5](https://kie.ai/seedance-2-5)
- [RD] Top-up sizes: the billing page's text resources say "PayPal is available for the $5 and $50 packs", "depending on the SKU we offer 5% or 10% bonus credits", and list corporate-transfer SKUs of ¥36 for 1,000 credits, ¥180 for 5,000, ¥360 for 10,000, ¥3,600 for 105,000 and ¥9,000 for 275,000. The purchase screen itself is behind login. — [kie.ai billing](https://kie.ai/billing)
- [RD] Operator: "Kie.ai is operated by NEXUSAI SERVICES LLC. Address: 118 Krameria St, Denver, CO 80220, United States." Support is by email plus "a private VIP support channel on Discord or Telegram". — [kie.ai about](https://kie.ai/about); [kie.ai contact](https://kie.ai/contact)
- [RD] Terms of Use (effective 1 Aug 2025, last updated 26 Oct 2026, Colorado law): "Purchased tokens (credits) never expire, and refunds are also supported if needed." "Payments may be collected by NEXUSAI SERVICES LLC or, on its behalf, by INNOLEAP AI LLC, and either company name may appear on your payment statement." The service is provided "as is" and the company "may suspend or terminate your access to the Website at any time, without notice or liability, for any reason". — [kie.ai terms](https://kie.ai/terms-of-use)
- [RD] Refund policy: refunds are requested by email with the order number and reason; "our support team will review it and reply by email". No time limit or conditions are stated. — [kie.ai refund policy](https://kie.ai/refund-policy)
- [RD] Payment routing: PayPal payments go through a different merchant: "You will be redirected to MusicHero's PayPal merchant to complete the payment. MusicHero is our payment merchant". The billing resources also mention WeChat Pay, corporate transfer arranged through a WeChat contact, and Chinese VAT invoices (fapiao). — [kie.ai billing](https://kie.ai/billing)
- [RD] Usability: "Playground – test every model in your browser before writing code." Model pages have a Playground tab with a form. — [kie.ai about](https://kie.ai/about); [kie.ai Kling 4.0 Flash](https://kie.ai/kling-4-0-flash)

**Table 3a. kie.ai image-to-video prices (no video input) versus fal.** kie.ai figures [RD] from the linked model pages; fal figures from Table 2a; "difference" is my calculation.

| Model | kie.ai price per second | fal price per second | kie.ai vs fal |
|---|---|---|---|
| [Seedance 2.5](https://kie.ai/seedance-2-5) | $0.140 (480p), $0.315 (720p), $0.790 (1080p); 28 / 63 / 158 credits; "prices are currently in beta and may be adjusted" | $0.2205 / $0.4730 / $1.164 | -36% / -33% / -32% |
| [Seedance 2.5 Flash](https://kie.ai/seedance-2-5-flash) | $0.0925 (480p), $0.205 (720p) | $0.1442 / $0.3094 | -36% / -34% |
| [Seedance 2.0](https://kie.ai/seedance-2-0) | $0.095 (480p), $0.205 (720p), $0.51 (1080p), $1.04 (4K); Fast $0.059 / $0.124 | $0.3024 (720p); Fast $0.2419 | -32%; Fast -49% |
| [Seedance 2.0 Mini](https://kie.ai/seedance-2-0-mini) | $0.019 (480p), $0.041 (720p) | $0.0721 / $0.1547 | -74% |
| [Kling 4.0](https://kie.ai/kling-4-0) | $0.1425 (720p), $0.2125 (1080p); 10 s at 1080p = $2.125 | $0.157 / $0.235 | -9% / -10% |
| [Kling 4.0 Flash](https://kie.ai/kling-4-0-flash) | $0.085 (720p, 3-20 s) | $0.094 | -10% |
| [Kling 3.0](https://kie.ai/kling-3-0) | Standard 720p $0.0755 without audio, $0.1135 with; Pro 1080p $0.101 / $0.151; 4K $0.3775; "about 10% below Kling's official pricing" | $0.084 / $0.126; $0.112 / $0.168 | -10% |
| [Kling 3.0 Turbo](https://kie.ai/kling-3-0-turbo), [Kling O3](https://kie.ai/kling-o3) | Turbo $0.101 (720p), $0.126 (1080p); O3 720p $0.0755 / $0.101, 1080p $0.101 / $0.126 | Turbo $0.112 / $0.14; O3 $0.084 / $0.112, $0.112 / $0.14 | -10% |
| [Veo 3.1](https://kie.ai/veo-3-1) (priced per video, length not stated in the price card) | Lite $0.15 (720p), $0.175 (1080p), $0.75 (4K); Fast $0.30 / $0.325 / $0.90; Quality $1.25 / $1.275 / $1.85 | 8 s with audio: Lite $0.40, Fast $1.20, standard $3.20 | -61% to -75% if kie's video is 8 s with audio (not confirmed) |
| [Gemini Omni 1.2 Flash](https://kie.ai/gemini-omni-1-2-flash) | $0.02 (360p), $0.045 (720p), $0.05 (1080p), $0.11 (4K) | $0.0273 / $0.0819 / $0.1229 / $0.2457 | -27% / -45% / -59% / -55% |
| [Gemini Omni 1.1 Flash](https://kie.ai/gemini-omni-1-1-flash) | per video at 360p-1080p: $0.315 (4 s), $0.42 (6 s), $0.525 (8 s), $0.63 (10 s) | $0.10/s at 720p | 10 s: -37% |
| [MiniMax H3](https://kie.ai/minimax-h3) | $0.04 (768p), $0.065 (2K); "pricing is 50% of the official price"; first 5 input images free | $0.06 / $0.13 | -33% / -50% |
| [Wan 3.0](https://kie.ai/wan3.0-video) | $0.04 (480p), $0.08 (720p), $0.16 (1080p); "20% below official pricing" (page cites Alibaba Cloud Model Studio at $0.05 / $0.10 / $0.20, November 2026) | $0.05 / $0.10 / $0.20 | -20% |
| [Wan 3.0 Prime](https://kie.ai/wan3.0-video-prime) | $0.0612 / $0.126 / $0.252 | $0.068 / $0.14 / $0.28 | -10% |
| [Vidu Q4 Preview](https://kie.ai/vidu-q4) | $0.036 (540p), $0.076 (720p), $0.096 (1080p), $0.152 (2K), $0.312 (4K); "20% below official pricing" | $0.0315 / $0.0665 / $0.084 / $0.133 / $0.273 | +14% (fal is cheaper) |
| [Hailuo 2.3](https://kie.ai/hailuo-2-3) (older MiniMax model, per video) | Standard 6 s 768p $0.15, 10 s 768p $0.26, 6 s 1080p $0.26; Pro 6 s 768p $0.22, 6 s 1080p $0.39 | not compared | |
| [Happy Horse 1.1](https://kie.ai/happyhorse-1-1) | $0.1125 (720p), $0.145 (1080p) | $0.14 / $0.18 | -20% |
| [PixVerse V6](https://kie.ai/pixverse-v6) | 720p $0.036 without audio, $0.048 with; 1080p $0.072 / $0.092 | $0.045 / $0.060; $0.090 / $0.115 | -20% |
| [Grok Imagine Video 1.5](https://kie.ai/grok-imagine-video-1.5) | $0.012 (480p), $0.0225 (720p), $0.04 (1080p); "approximately 84% below official pricing" | $0.08 / $0.14 / $0.25 | -84% to -85% |

- [RD] kie.ai applies a lower per-second rate when a reference video is uploaded but then bills input plus output seconds (Seedance 2.5 with video: $0.085 / $0.19 / $0.475). Every pricing card adds that "high-tier top-ups include a +10% bonus". No HeyGen Video 1, MiniMax H3 Max or Pika H3 Flex entry appears in kie.ai's 144-model index. — [kie.ai Seedance 2.5](https://kie.ai/seedance-2-5); [kie.ai pricing](https://kie.ai/pricing)

**Table 3b. kie.ai image prices per image.** All [RD]; fal comparison from Table 2b.

| Model | kie.ai | fal | Difference |
|---|---|---|---|
| [Nano Banana 2.1](https://kie.ai/nano-banana-2-1) | $0.02 (1K), $0.03 (2K), $0.045 (4K); "1K/2K 40% and 4K 60% below official pricing" | about $0.040 / $0.059 / $0.134 | -50% / -49% / -66% |
| [Nano Banana 2](https://kie.ai/nano-banana-2) | $0.04 (1K), $0.06 (2K), $0.09 (4K) | $0.08 / $0.12 / $0.16 | -50% / -50% / -44% |
| [Nano Banana Pro](https://kie.ai/nano-banana-pro) | $0.09 (1K/2K), $0.12 (4K) | $0.15 / $0.30 | -40% / -60% |
| [Nano Banana 2 Lite](https://kie.ai/nano-banana-2-lite) | $0.02 (1K only) | token-billed | |
| [Seedream 5.5](https://kie.ai/seedream-5-5) | $0.018 (1K/1.5K), $0.0315 (2K); input image $0.0072; "10% below official pricing" | $0.03 / $0.0405; input $0.012 | -40% / -22% |
| [Seedream 5.0 Pro](https://kie.ai/seedream-5-0-pro) | $0.035 (1K), $0.07 (2K) | $0.0675 / $0.135 (tentative) | -48% |
| [GPT Image 2.6](https://kie.ai/gpt-image-2-6) | Flare / Sunburst token-billed: image output $27.00 per million tokens ("10% below official pricing"); an "Economy" variant has a flat price from $0.025 per image (1K only) | image output $30 per million tokens | -10% on tokens |
| [GPT Image 2.5](https://kie.ai/gpt-image-2-5), [GPT Image 2](https://kie.ai/gpt-image-2) | $0.03 (1K), $0.05 (2K), $0.08 (4K) flat | GPT Image 2 at 1024x1024: $0.006-$0.211 by quality | quality level on kie.ai not stated on the card |
| [FLUX 3 Klein](https://kie.ai/flux-3) | $0.008 (1K), $0.0125 (2K), $0.0325 (4K) | FLUX 3 Image (full model) $0.048 per megapixel | different model tier |

**Reliability and legitimacy (web search; none of these pages was opened)**
- [SS, third-party review checked 21 Oct 2026] kie.ai's Trustpilot profile "scores 2.1 out of 5 from 16 reviews", with complaints about jobs "stuck at 99% while credits are used" and hours of HTTP 500 errors; the review notes the sample is small and unverified, that kie.ai "does not say how it obtains that access", that a public status page is missing, and that kie.ai's "Official / Fal Price" discount column often uses fal's price, which inflates some savings claims. — [gengrades](https://gengrades.com/kie-ai)
- [SS] Regional Trustpilot pages cached about a year ago showed 2.8 from 3 reviews and 2.9 from 2 reviews, all one-star, about stalled generations, error messages and difficulty getting refunds or support. — [Trustpilot, kie.ai (NZ page)](https://nz.trustpilot.com/review/kie.ai)
- [SS, third party; some of these sites compete with or earn from the services they review] One review calls kie.ai "a legitimate API reseller" with site-trust scanners rating it around 80/100, but says Trustpilot sits "around 2.5 out of 5 from a small pool", reviewers describe recurring API errors and downtime, and kie.ai's own documentation admits stability may run below official providers; secondhand mentions of r/n8n threads about error rates and a platform-wide outage could not be verified. — [aireiter](https://aireiter.com/blog/kie-ai-review-2026); [bitdoze](https://www.bitdoze.com/kie-ai-review/)
- [SS, third party] kie.ai is described as "a small company registered in Colorado in 2024" with "no formal SLA and no published SOC2 or GDPR documentation"; the same review says its Colorado registration showed as noncompliant at the end of 2025, which was not verified against a state record. — [vantaige](https://vantaige.io/ai-tool/kie-ai)
- [SS] kie.ai's own Veo documentation is reported to mention a fallback to a backup model if the official Veo service is unavailable. — [kie.ai docs mirror](https://kieai.mintlify.app/veo3-api/generate-veo-3-video)

**Verdicts on first-round figures**
- CONFIRMS: credit value ($0.005), no subscription, credits never expire, failed tasks not charged, 80 free credits, +10% bonus at $1,250; Veo 3.1 per-video prices (all nine); Kling 3.0 Standard and Pro prices.
- CORRECTS: the first round said Seedance 2.5 was not publicly priced on kie.ai. It is: $0.14 / $0.315 / $0.79 per second.
- NEW: operator identity, payment merchants, the $5 smallest pack, Kling 4.0, MiniMax H3, Wan 3.0, Gemini Omni 1.2 Flash, Vidu Q4 and image prices, and the reliability evidence.

### Inferences
- The discounts fall into three groups. About 10% under list (Kling family) is what a volume reseller can plausibly pass on. 20-36% under fal (Wan 3.0, MiniMax H3, Seedance 2.5) is still explicable, because fal itself prices Seedance well above ByteDance's own API (first round: 82-114% above; AA's maker price for Seedance 2.5 at 1080p is $0.569/s against fal's $1.164/s and kie.ai's $0.79/s). Discounts of 45-85% below the maker's list price (Gemini Omni Flash 1.2, Nano Banana, Grok Imagine Video, Veo) cannot come from ordinary resale margins; kie.ai does not explain them. Possible explanations (regional pricing, committed-volume contracts, promotional credits, or unofficial access routes) are speculation on my part; the practical consequence is a higher risk that such a model slows down, changes or disappears without notice.
- Corporate signals are mixed rather than alarming: a named US LLC with a street address and published terms, but payments collected by two other entities (INNOLEAP AI LLC, "MusicHero"), China-facing payment options, a vague refund rule and the right to terminate accounts at will. For a solo creator the sensible safeguard is to keep balances small ($5-$50 packs), since "credits never expire" is only worth as much as the operator's continuity.
- At the budget end the absolute saving from kie.ai is small: MiniMax H3 768p is $0.04/s against $0.06/s on fal, which is $6-$18 a month on 60-180 five-second generations. The saving is material only for Seedance 2.5 ($47-$142 a month at the same volumes at 720p).
- kie.ai is not uniformly cheapest: Vidu Q4 is 14% dearer than on fal, and it does not list HeyGen Video 1, which is the cheapest near-frontier image-to-video model on fal.

### Gaps
- No primary evidence was found on how kie.ai sources Google, xAI or ByteDance capacity, or on its uptime; docs.kie.ai (which reportedly carries a success-rate figure and a stability disclaimer) is a blocked host.
- The length and audio status of kie.ai's per-video Veo 3.1 prices were not stated in the price card.
- The full USD pack ladder and the current Trustpilot score could not be read directly; the 2.1/5 figure comes from a third-party page.
- Commercial-use terms for outputs are not stated in the kie.ai pages read; they presumably follow each model maker's terms.

---

## 4. Higgsfield (higgsfield.ai): plans, prices, credits, credit cost per clip, "unlimited" fine print, commercial rights, documented complaints

### Takeaway
Higgsfield's own posts from 13 October to 10 November 2026 consistently give Starter $15/month (200 credits), Plus $49 (1,000) and Ultra $129 (3,000; $99/month on annual billing), with a 5-second Seedance 2.5 clip costing 35 credits at 720p ($1.72 on Plus) and 80 at 1080p ($3.92); the live plan table could not be rendered and the site is running a "Black Friday 65% off" sale from 16 to 18 November. "Unlimited" on Higgsfield is a set of image models plus short time-limited windows on video models, run in a separate slower queue, one video at a time, subject to fair-use throttling; and the refund rule (7 days, only if no credit has been used, renewals excluded) matches the dominant theme of user complaints.

### Cited Findings

**Plans and prices**
- [RD, vendor blog dated 24 Oct 2026, "prices verified October 2026 on the Higgsfield pricing page"] Individual plans, monthly billing: Free $0 (no credits, "a limited set" of models); Starter $15/month, 200 credits, "selected models"; Plus $49/month, 1,000 credits, every model; Ultra $129/month, 3,000 credits, every model. Business: Team $79 per seat/month (1,000 credits per seat, 2-9 members); Scale $215 per seat/month (2,500 per seat, 5-15 members). "You can pay monthly or annually." — [Higgsfield pricing explained](https://higgsfield.ai/blog/higgsfield-pricing-explained)
- [RD, vendor blogs] The same three prices and credit amounts appear in posts dated 13 Oct and 18 Oct 2026, and the 10 Nov 2026 post repeats Plus at $49 for 1,000 credits; Ultra is "3,000 credits, scalable up to 9,000" with "a slider", and "Ultra with the slider at 6,000 credits costs $250". — [Higgsfield API vs subscriptions](https://higgsfield.ai/blog/ai-video-api-pricing-vs-subscriptions); [Higgsfield all-in-one post](https://higgsfield.ai/blog/best-all-in-one-subscription-ai-images-video); [Higgsfield Seedance 2.5 pricing](https://higgsfield.ai/blog/seedance-2-5-pricing-2026)
- [RD, vendor blog dated 11 Sep 2026] Annual billing: "Plus $49/mo; Ultra annual $99/mo"; "$129/mo, $99/mo annual". No first-party page read today states an annual price for Plus. — [Higgsfield annual unlimited plans](https://higgsfield.ai/blog/annual-unlimited-ai-video-plans)
- [RD, competitor content dated about 23 Oct 2026, Higgsfield data "captured August 31, 2026"] Krea's guide gives a different ladder: Starter $19 (270 credits), Plus $59 monthly or $47 annual (1,200 credits), Ultra $129 monthly or $99 annual (3,000), auto-refill at $1 per 20 credits, and says the pricing page "defaults to annual billing". — [Krea on Higgsfield pricing](https://www.krea.ai/blog/higgsfield-pricing-explained-2026-unlimited-credits-and-real-monthly-costs)
- [SS, third parties] One review says a pricing-page snapshot from early October showed Starter $19 / 270 credits and Plus $59 / 1,200, before the 24 October explainer listed $15 / 200 and $49 / 1,000; a Korean guide dated 25 Oct 2026 still gives $19, $59 ($47 annual) and $129 ($99 annual). — [diyai](https://diyai.io/ai-tools/video-generation/higgsfield-pricing/); [wikidocs](https://wikidocs.net/blog/@ai_agent_skill/34515/)
- [RD] The live pricing page delivers no plan table without JavaScript. Its embedded data shows a campaign "sale_11_11" active from 16 Nov to 18 Nov 2026 with banners "Black Friday 65% OFF", "Up to 65% OFF premium plans" and "Get up to 63% off business plans & up to 30 days of unlimited Seedance 2.5". The same data holds 16 time-boxed campaign records dated from 28 Jul to 18 Nov 2026 (15 earlier ones plus this sale), with names such as "seedance_2_5_sale", "unlim_marketplace_bundles", "kling_4_release" and "plan_free_gens". — [Higgsfield pricing](https://higgsfield.ai/pricing)
- [RD, vendor blog dated 11 Nov 2026] The "11.11" offer: annual plans "discounted by up to 60%, with the largest discount on Ultra 9K"; a 3-day $0 trial through Higgsfield MCP that "renews automatically on Ultra 3K at a discounted price". — [Higgsfield 11.11 deals](https://higgsfield.ai/blog/higgsfield-11-11-deals)
- [RD] Plan differences: video jobs at once 1 (Free) / 2 (Starter) / 6 (Plus) / 8 (Ultra); Start & End Frame control, Higgsfield Speak and UGC builder only on Plus and Ultra; "Seedance 2.5, Seedance 2.0, Veo, Kling 3.0 at 1080p" need Plus or Ultra; Starter includes Seedance 2.0 Fast and Mini. — [Higgsfield pricing explained](https://higgsfield.ai/blog/higgsfield-pricing-explained); [Higgsfield all-in-one post](https://higgsfield.ai/blog/best-all-in-one-subscription-ai-images-video)

**Credit rules and credit cost per clip**
- [RD] Credit costs "taken from the Higgsfield pricing page and interface in October 2026": Seedance 2.5, 5 s: 35 credits at 720p, 80 at 1080p; 30 s at 720p: 210. Seedance 2.0, 5 s: 30 (720p), 60 (1080p), 130 (4K). Veo 3 Fast with audio, 8 s 720p: about 22; Veo 3 with audio, 8 s 720p: about 58. Genjutsu Lite 15 s 720p: 32. Nano Banana Pro image: 2 (4K: 4); FLUX.2 Pro image: 1. On Plus ($0.049 per credit) a 5 s Seedance 2.5 clip is about $1.72 at 720p and $3.92 at 1080p; 1,000 credits cover "28 five-second Seedance 2.5 clips at 720p (or 12 at 1080p)". — [Higgsfield pricing explained](https://higgsfield.ai/blog/higgsfield-pricing-explained)
- [RD] Seedance 2.5, 10 s: 70 credits at 720p ($3.43 on Plus) and 30 credits at 480p ($1.47); Seedance 2.0, 10 s 720p: 60 credits. — [Higgsfield Seedance 2.5 pricing](https://higgsfield.ai/blog/seedance-2-5-pricing-2026)
- [RD] Kling 3.0 at 8 s and 720p "costs 16 credits per generation" on the website; the separate Higgsfield API charges $0.084 per second for it. — [Higgsfield API vs subscriptions](https://higgsfield.ai/blog/ai-video-api-pricing-vs-subscriptions)
- [RD] Kling 4.0: the post's table says 5 s = 13.75 credits at 720p ($0.67) and 20 at 1080p ($0.98), 30 s = 82.5 and 120; the FAQ at the end of the same post says "A 5-second Kling 4.0 video costs 25 credits at 720p or 37.5 credits at 1080p. A 30-second video costs 150 credits at 720p or 225 credits at 1080p." The two statements conflict. — [Kling 4.0 on Higgsfield](https://higgsfield.ai/blog/kling-4-0-on-higgsfield)
- [RD] "If a generation fails, the credits are usually returned automatically. If a generation finishes, the credits aren't returned, even if you don't like the result." "On monthly billing, credits refresh on your billing date. On annual billing, they refresh every 30 days. Unused credits don't roll over." Credit packs and Auto-Refill need an active subscription (Auto-Refill not on Starter) and "expire 90 days after purchase". The API has its own dollar balance. — [Higgsfield pricing explained](https://higgsfield.ai/blog/higgsfield-pricing-explained)
- [RD] Free plan: "doesn't include monthly credits"; generations "can carry a visible Higgsfield watermark"; one generation at a time. Paid plans: no visible watermark. — [Higgsfield pricing explained](https://higgsfield.ai/blog/higgsfield-pricing-explained)
- [RD, vendor's own estimate of retries] "At three to five attempts per usable clip, a regular workload of 30 clips a month costs $324 to $540 in credits at Higgsfield's Seedance 2.5 rate." — [Higgsfield credits vs unlimited](https://higgsfield.ai/blog/credits-vs-unlimited-ai-video-generation)

**Exact fine print of "unlimited"**
- [RD, Terms of Use, last updated 23 Oct 2026, section 10.6, quoted in full] "To ensure a stable and fair experience for all users, model usage under subscription tiers marketed as 'Unlimited' is subject to Company's fair-use limits and the dynamic speed and concurrency limitations described below. Company may restrict, suspend, throttle, or place on a slower processing queue usage that is automated or materially exceeds typical individual use, in order to protect Service quality for other users. Unlimited models operate on a dedicated processing queue, separate from the priority queue used for credit-based generations. During periods of high demand, generation speeds may vary and additional concurrency limits may apply. Processing speed and parallel generation capacity are not guaranteed and may dynamically adjust based on overall platform usage." — [Higgsfield Terms of Use](https://higgsfield.ai/terms-of-use-agreement)
- [RD] "Unlimited means some models don't charge credits while the Unlimited toggle is on." Two kinds exist: "365-day Unlimited Models" and "7-day Unlimited on selected models, a shorter access window. When it ends, those models charge credits again." The 365-day set on Plus and Ultra is image models only: Seedream 5.0 Lite (2K/3K), FLUX.2 Pro (1K), Seedream 4.5 (2K/4K), Nano Banana, Kling O1 Image and GPT Image; Starter gets Seedream 5.0 Lite and FLUX.2 Pro (1K). 7-day Unlimited: Plus monthly Nano Banana 2 (1K/2K); Plus annual adds Kling 3.0 (720p, 5 s); Ultra monthly Nano Banana 2 and Nano Banana Pro; Ultra annual adds Kling 3.0 (720p, 5 s). — [Higgsfield pricing explained](https://higgsfield.ai/blog/higgsfield-pricing-explained)
- [RD] "The Unlimited bonuses on plans work only on higgsfield.ai. Generations through MCP, CLI, Canvas, or Supercomputer deduct credits"; Marketing Studio also always draws on credits. "When a bonus period ends, it does not renew." — [Higgsfield 11.11 deals](https://higgsfield.ai/blog/higgsfield-11-11-deals); [Higgsfield all-in-one post](https://higgsfield.ai/blog/best-all-in-one-subscription-ai-images-video)
- [RD] Concurrency under Unlimited: "Two generations at a time, shared across all unlimited image models. One generation at a time across unlimited video models." "A plan's 'Unlimited paid parallel generations' feature does not remove the concurrency limits for the Unlimited bonus." — [Higgsfield 7-day unlimited bonus](https://higgsfield.ai/blog/higgsfield-7-day-unlimited-bonus)
- [RD] Promotional video windows seen: Plus monthly bought by 14 Nov got 7 days of Unlimited Seedance 2.5 "at up to 20 seconds and 480p"; Ultra monthly and annual plans 14 days; Ultra annual had the highest resolution at 1080p. — [Higgsfield 11.11 deals](https://higgsfield.ai/blog/higgsfield-11-11-deals)
- [RD] Paid passes: the Unlimited Models Marketplace "sells 1, 3, and 7-day passes per model, from $7 for a 1-day pass to $1,035 for a 7-day all-models pass", "in the standard queue, with resolution and duration caps set per model". — [Higgsfield credits vs unlimited](https://higgsfield.ai/blog/credits-vs-unlimited-ai-video-generation)

**Refunds, renewal and rights (Terms of Use, last updated 23 Oct 2026)**
- [RD] Refunds (section 9.3): "You may request a refund within seven (7) days of your initial purchase ... provided no Credits ... have been used." "Refunds apply only to initial purchases, not renewals, and are subject to a service fee not exceeding six percent (6%) of the initial fee where permitted by law. Otherwise, all amounts paid are non-refundable." Credit packs: refundable only within 7 days and only if no credits from the pack were used. — [Higgsfield Terms of Use](https://higgsfield.ai/terms-of-use-agreement)
- [RD] EU/EEA and UK consumers (section 17.2) have a 14-day right of withdrawal, but "you lose your right of withdrawal once we begin supplying" digital content such as credits or outputs, and must pay for credits already used. — [Higgsfield Terms of Use](https://higgsfield.ai/terms-of-use-agreement)
- [RD] Subscriptions renew automatically "at Company's then-current price"; the company "will provide at least thirty (30) days' advance notice of any price increase"; free trials and promotional prices "automatically convert to a paid Subscription and renew at Company's then-current standard price"; "no prorated refunds ... for the current term"; "unused Credits expire upon Account cancellation"; disputes go to binding arbitration with a class-action waiver (30-day opt-out). If the company "materially and adversely degrades the overall functionality of a paid plan", the user may cancel and receive a pro-rata refund. — [Higgsfield Terms of Use](https://higgsfield.ai/terms-of-use-agreement)
- [RD] Rights: "Paid plans include commercial use." Terms: "Company does not claim ownership of any of your Inputs or Outputs, nor does it restrict your commercial use of Outputs"; rights in exported outputs survive cancellation; the company "may embed machine-readable watermarks, secure metadata, or content-provenance signals (such as those based on the C2PA / Content Credentials standard) into Outputs". — [Higgsfield pricing explained](https://higgsfield.ai/blog/higgsfield-pricing-explained); [Higgsfield Terms of Use](https://higgsfield.ai/terms-of-use-agreement)

**Documented complaints (web search; pages not opened)**
- [SS] Trustpilot shows a TrustScore of 4.0 from about 5,517 reviews (US page, snapshot about a day old); one snapshot showed about 62% five-star and 19% one-star reviews. — [Trustpilot, Higgsfield AI](https://www.trustpilot.com/review/higgsfield.ai)
- [SS] Negative Trustpilot reviews from May to July 2026 describe charges after cancellation (one "billed two hours after cancelling" and refused a refund) and refunds rejected under the initial-purchase-only rule; other reviewers report quick refunds. Reviews also say Unlimited runs "ONE generation at a time" and that unlimited Nano Banana at 2K is "so slow that it becomes almost unusable". — [Trustpilot, Higgsfield AI](https://www.trustpilot.com/review/higgsfield.ai)
- [SS] Better Business Bureau complaints in 2026 describe refunds refused because credits had been used or because the charge was a renewal; in one case the company later said it refunded. — [BBB, Higgsfield AI complaints](https://www.bbb.org/us/ca/san-francisco/profile/artificial-intelligence/higgsfield-ai-1116-977987/complaints)
- [SS, press] The Register (6 Feb 2026) reported an ex-user's criticism that refunds are effectively unavailable once the service has been used, in an article about a backlash over a company post on replacing creative jobs. — [The Register](https://www.theregister.com/2026/02/06/higgsfield_ai_job_loss/)
- [SS, third party] A March 2026 r/StableDiffusion thread, as reported by a news aggregator, described a $350+ annual charge refunded only after the user threatened a chargeback. Two single-purpose complaint sites exist (cancelhiggsfield.com, higgsfieldscammedme.com). An article alleging a lawsuit over holiday subscriptions had no court record or mainstream confirmation. — [The Neural Feed](https://theneuralfeed.com/article/stay-away-from-higgsfield-ai-total-predatory-bs-with-their-refunds/3tKtWyUd); [cancelhiggsfield.com](https://cancelhiggsfield.com/); [quasa.io](https://quasa.io/media/higgsfield-ai-and-the-christmas-grinch-unraveling-the-holiday-subscription-scandal)
- [SS, vendor and third party] Higgsfield's own help content states "Unlimited generations run in the standard queue, while credit-based generations always run in the priority queue"; third-party explainers describe the unlimited queue slowing with use and "crawling for hours" under load during an August campaign. Several of these explainers are affiliate or competitor content. — [Higgsfield on Seedance Unlimited changes](https://geo.higgsfield.ai/blog/higgsfield-seedance-unlimited-plan-changes); [aireiter](https://aireiter.com/blog/higgsfield-free-unlimited-explained); [Zemith, competitor](https://www.zemith.com/en/learn/higgsfield-review)

**Verdicts on first-round figures**
- CONFIRMS: price set (a) Starter $15 / 200, Plus $49 / 1,000, Ultra $129 / 3,000 is what Higgsfield's own posts state from 13 Oct to 10 Nov 2026; Ultra annual $99/month; Seedance 2.5 10 s 720p = 70 credits; Kling 3.0 8 s 720p = 16 credits; Marketplace passes from $7 to $1,035; unlimited only on the web app; free plan has no credits.
- CONTRADICTS / unresolved: price set (b) (Starter $19 / 270, Plus $59 / 1,200) is found only in competitor and third-party pages based on August to early-October captures; it may be an older ladder or a regional variant. The live table could not be read, so which set a buyer sees on 17 Nov 2026 (during a sale) is unverified.
- CORRECTS: Kling 4.0 "10 s at 1080p = 32.5 credits" is not supported; Higgsfield's own post gives 20 credits per 5 s at 1080p in one place and 37.5 in another (40 or 75 per 10 s). Veo 3.1 "8 s at 720p = 80 credits" was not found; the October post lists Veo 3 at about 58 credits. "About 17 Seedance clips on Plus" assumed 1,200 credits; with 1,000 credits it is 14 ten-second 720p clips.
- CORRECTS: standing 7-day unlimited windows cover image models (plus Kling 3.0 at 720p, 5 s on annual plans); unlimited Seedance 2.5 appears only in time-limited promotions.

### Inferences
- Dollar cost per 5-second generation at the first-party prices (my calculation): Seedance 2.5 720p $2.62 on Starter (if it were available there; it is not), $1.72 on Plus, $1.50 on Ultra monthly, $1.16 on Ultra annual; Seedance 2.5 1080p $3.92 / $3.44 / $2.64; Kling 3.0 720p (10 credits per 5 s, scaled from 16 per 8 s) $0.75 on Starter, $0.49 on Plus; Kling 4.0 720p $0.67-$1.23 on Plus depending on which of the two published credit figures is right.
- Plus covers 28 five-second Seedance 2.5 generations a month at 720p, which is 9 usable clips at 3 generations each; Ultra covers 85 generations (28 usable clips). The 20-60 clip workload on Seedance 2.5 therefore needs Ultra at minimum, and 60 usable clips need about 6,300 credits (Ultra at the 6,000 setting, reported at $250, plus a pack).
- Higgsfield's constant promotions (16 time-boxed campaign records in the page data since late July) and the two published credit figures for Kling 4.0 mean the price actually paid can only be known at the Generate button. Buying an annual plan during a sale locks in a year under a refund rule that ends the moment one credit is spent.
- The Trustpilot score of 4.0 is not reassuring by itself: roughly one review in five is one-star and the themes (post-cancellation charges, refused refunds, slow unlimited queue) match exactly what the Terms permit.

### Gaps
- The live plan table, the annual price of Plus, current sale prices, and the model list available on Starter could not be read (JavaScript shell).
- Credit costs for Veo 3.1, Gemini Omni Flash and MiniMax H3 on Higgsfield were not found in the posts read.
- Reddit threads, BBB complaint texts and Trustpilot reviews were not opened; counts and quotes come from search summaries.
- Whether prices differ by country (first round: "prices vary by country and exclude tax") was not re-checked.

---

## 5. Krea (www.krea.ai): plans, prices, compute units, per-clip cost, commercial rights

### Takeaway
Krea's paid plans are Basic (5,000 compute units, $9 monthly or $5/month billed yearly), Pro (20,000 units, $35 or $21) and Max (selector from 40,000 units at $70 or $42 to 60,000 at $105 or $63 and beyond), all at the same $0.00175 per unit on monthly billing and $0.00105 on yearly billing, all with a commercial licence. A 5-second 720p clip costs about 856 units for Seedance 2.5 ($1.50 monthly, $0.90 yearly), 581 for Kling 4.0 ($1.02 / $0.61) and a 5-second 480p MiniMax H3 Max clip about 130 units ($0.23 / $0.14), which makes Krea the cheapest verified subscription route to Seedance 2.5.

### Cited Findings
- [RD] Plans (toggle "Monthly / Yearly, 40% off"): Free "100 units / day", $0, "no credit card required"; Basic "5,000 units / month", $9 monthly or $5/month yearly ("Save $48"; the comparison table shows $5.25); Pro, "Most popular", "20,000 units / month", $35 or $21 ("Save $168"); Max with a size selector 40k / 60k / 80k / 100k: 60,000 units at $105 or $63 ("Save $504"), 40,000 units at $70 or $42 ("Save $336"); Business 80,000 units at $200 or $160 with up to 50 seats; Enterprise custom. — [Krea pricing](https://www.krea.ai/pricing)
- [RD] Plan-card claims (vendor marketing): Basic "~200 Nano Banana 2.1 generations, ~16 Seedance 2.5 videos"; Pro "~803 Nano Banana 2.1 generations, ~65 Seedance 2.5 videos"; Max 60k "~197 Seedance 2.5 videos". The detailed comparison table on the same page gives, for "Seedance 2.5, 5s, 720p, no video reference", about 5 / 23 / 46 videos on Basic / Pro / Max 40k. — [Krea pricing](https://www.krea.ai/pricing)
- [RD] Features: Basic has "All image models" and "Selected video models"; Pro and Max have "All video models". In the comparison table every listed video model except Veo 3.1 (standard) shows a generation count for Basic. Video concurrency is 2 (Basic), 4 (Pro), 8 (Max). The Free column shows a video count for only one model (LTX-2 19B, about 2 videos a day at 5 s, 512p). — [Krea pricing](https://www.krea.ai/pricing)
- [RD] "Basic, Pro, and Max plans allocate compute units monthly and they do not roll over"; "unused units expire at the end of each billing cycle". One-time compute packs of 2,000, 5,000, 10,000, 24,000 and 50,000 units are "valid for 90 days" (pack prices need sign-in). Plan changes are prorated. — [Krea pricing](https://www.krea.ai/pricing)
- [RD] "Yes, Basic, Pro, Max, Business, and Enterprise plans include a commercial license that allows you to use all generated content for commercial purposes without restrictions." The Free plan is not in that list. — [Krea pricing](https://www.krea.ai/pricing)
- [RD] The plan-picker tool on the page states "About 581 units per video and 78 per image" for "~40 Kling 4.0 videos (23,240 units)" and "~60 Nano Banana Pro images (4,680 units)". — [Krea pricing](https://www.krea.ai/pricing)
- [RD, vendor blog dated 26 Oct 2026] Seedance 2.5 on Krea: "A 5-second clip costs 856 compute units (CU) at 720p, about 380 CU at 480p and about 2,106 CU at 1080p" (about 76 / 171 / 421 CU per second); a 30-second take is about 2,282 / 5,136 / 12,636 CU; "Draft mode is billed at the 480p rate". — [Krea Seedance 2.5 pricing](https://www.krea.ai/blog/seedance-2-5-pricing-cost-per-video)
- [RD] Krea's separate API lists Kling 3.0 "from $0.084 per second", Kling 4.0 "from $0.157 per second", Veo 3.1 "from $0.80 per video", Wan 3.0 "from $0.075 per second", Seedance 2.0 "from $0.0809 per second", Runway Gen-4.5 "$0.12 per second", MiniMax H3 Max "from $0.175 per video", Nano Banana 2.1 "from $0.045 per image", Nano Banana Pro "from $0.15 per image". — [Krea API](https://www.krea.ai/features/api)

**Table 5a. Krea compute units per generation, derived from the generation counts in the comparison table (units = 20,000 / Pro count), and dollars per generation on Pro.** Counts are [RD] — [Krea pricing](https://www.krea.ai/pricing); units and dollars are my calculation ($0.00175 per unit monthly, $0.00105 yearly).

| Model and setting as listed by Krea | Pro count per month | Units per generation | $ monthly billing | $ yearly billing |
|---|---|---|---|---|
| Seedance 2.5, 5 s, 720p, no video reference | ~23 | ~870 (blog: 856) | 1.50 | 0.90 |
| Seedance 2.5, 5 s, 480p (blog) | ~52 | ~380 | 0.67 | 0.40 |
| Seedance 2.0, 4 s, 480p, video reference | ~83 | ~241 | 0.42 | 0.25 |
| Seedance 2.0 Fast / Mini, 4 s, 480p | ~104 / ~164 | ~192 / ~122 | 0.34 / 0.21 | 0.20 / 0.13 |
| Kling 4.0, 3 s, 720p (5 s = 581 units per the plan picker) | ~57 | ~351 | 0.61 (5 s: 1.02) | 0.37 (5 s: 0.61) |
| Kling 4.0 Flash, 3 s | ~95 | ~211 | 0.37 | 0.22 |
| Kling 3.0, 3 s, standard mode, audio off | ~107 | ~187 | 0.33 | 0.20 |
| Veo 3.1, 4 s, 720p, audio off (no Basic count) | ~33 | ~606 | 1.06 | 0.64 |
| Veo 3.1 Fast / Lite, 4 s, 720p | ~84 / ~225 | ~238 / ~89 | 0.42 / 0.16 | 0.25 / 0.09 |
| Gemini Omni Flash 1.2, 3 s, 360p | ~450 | ~44 | 0.08 | 0.05 |
| MiniMax H3 Max, 5 s, 480p | ~154 | ~130 | 0.23 | 0.14 |
| MiniMax H3 Max Turbo, 5 s, 480p | ~216 | ~93 | 0.16 | 0.10 |
| MiniMax H3, 5 s (resolution not stated) | ~41 | ~488 | 0.85 | 0.51 |
| Wan 3.0, 2 s, 480p | ~180 | ~111 | 0.19 | 0.12 |
| Hailuo 2.3, 6 s, 768p | ~96 | ~208 | 0.36 | 0.22 |
| Vidu Q3, 1 s, 540p | ~385 | ~52 | 0.09 | 0.05 |
| FLUX 3 Max, 5 s, 720p | ~31 | ~645 | 1.13 | 0.68 |
| Runway Gen-4.5, 2 s | ~112 | ~179 | 0.31 | 0.19 |
| Nano Banana 2.1, 1K image | ~803 | ~25 | 0.044 | 0.026 |
| Nano Banana Pro, 1K image | ~257 | ~78 | 0.136 | 0.082 |
| Seedream 5 Pro, 1.5K image | ~600 | ~33 | 0.058 | 0.035 |
| GPT Image 2.5 / 2.6 (Flare or Sunburst) image | ~157 | ~127 | 0.223 | 0.134 |
| Krea 3 image | ~1,111 | ~18 | 0.032 | 0.019 |

- [SS, mixed sources] Krea's Trustpilot score varies by regional page and date: 2.5 from 74 reviews (UK page), 3.5 from 129 (NZ page), and 3.6 from 183 with 33% one-star per a competitor's review dated 11 Nov 2026; recurring complaints concern compute units not matching the plan, charges after cancellation and slow support. — [Trustpilot, Krea](https://uk.trustpilot.com/review/krea.ai); [Zemith, competitor](https://www.zemith.com/en/learn/krea-review)

**Verdicts on first-round figures**
- CONFIRMS: Basic $9 / $5 with 5,000 units, Pro $35 / $21 with 20,000 units, commercial licence from Basic, Seedance 2.5 at 856 / about 380 / about 2,106 units, API prices for Kling 3.0 and Veo 3.1.
- CORRECTS: the Max conflict ("40,000 CU at $70" versus "$105") is a size selector: 40,000 units cost $70 monthly ($42 yearly) and 60,000 units cost $105 ($63). The Free plan is not strictly image-only: one video model (LTX-2 19B) shows about 2 videos a day.
- CORRECTS: "the full video catalog opens at Pro" is only partly supported; Basic already shows counts for Seedance 2.5, Kling 4.0 and MiniMax H3 Max, and only Veo 3.1 standard lacks one.
- NEW: unit costs for Kling 4.0, Veo 3.1, MiniMax H3 Max, Gemini Omni Flash 1.2, Wan 3.0 and Runway Gen-4.5 (first-round gap).

### Inferences
- Krea's headline "~65 Seedance 2.5 videos" on Pro equals about 308 units per video, which matches a 4-second clip at 480p (76 units per second); at the 5-second 720p setting a social creator would actually use, Pro yields 23 generations. The headline counts overstate practical output by a factor of about 2.8.
- The price per unit does not fall with plan size ($0.00175 monthly on Basic through Max; $0.00105 yearly), so the only discount lever is the 40% for yearly billing, and a creator loses nothing by starting on a small plan and adding 90-day compute packs if their price per unit is similar (pack prices were not visible).
- Per-clip prices listed at 2-4 seconds and 360p-480p make cross-model comparison on Krea awkward; scaling linearly to 5 s at 720p is an assumption that holds for Seedance 2.5 (171 units per second at 720p) but was not confirmed for other models.
- With 3 generations per usable clip at 5 s and 720p, Pro covers 7 usable Seedance 2.5 clips a month, Max 40k covers 15 and Max 60k covers 23; with two 480p drafts and one 720p final per clip (1,616 units) the same plans cover 12, 24 and 37 usable clips.

### Gaps
- Prices of compute packs and of Max at 80k and 100k were not visible without interaction; the list of "selected video models" on Basic is inferred from the table, not stated.
- Unit costs at 720p for MiniMax H3 Max, Gemini Omni Flash 1.2 and Wan 3.0 are not published on the pricing page (only 360p-480p settings).
- Refund terms and the meaning of "Unlimited relaxed generations" (a feature row whose per-plan ticks are icons) were not read; a Higgsfield post claims it covers only Krea's in-house image models — [Higgsfield all-in-one post, competitor](https://higgsfield.ai/blog/best-all-in-one-subscription-ai-images-video).

---

## 6. Magnific, formerly Freepik (www.magnific.com) and Artlist (artlist.io): plans and per-clip costs

### Takeaway
Magnific's pricing page was readable: Premium is $20 monthly ($14.50/month billed annually, 240,000 credits a year), Plus $45 ($33.75, 600,000) and Pro $110 ($82.50, 1.5 million) or $280 ($210, 4 million), and video is priced per second in credits worth about $0.001 each on monthly billing, so a 5-second clip costs $0.40 on MiniMax H3 Max 768p, $0.45 on Kling 3.0 Pro 1080p, $1.40 on Kling 4.0 1080p and $2.20 on Seedance 2.5 720p. Artlist's AI plans are confirmed at $19.99 / $39.99 / $69.99 monthly or $11.99 / $23.99 / $41.67 on annual billing for 16,500 / 40,000 / 80,000 credits, and its yearly AI Core plan includes credit-free "Unlimited" generation on MiniMax H3 Max and Wan 3.0, but only at 480p and 5 seconds.

### Cited Findings

**Magnific**
- [RD, embedded price data for country "US"] Individual plans: Premium $20.00 monthly (20,000 credits a month) or $174.00 a year (= $14.50/month, 240,000 credits a year, shown as 27% off); Plus (internal name "Premium+") $45.00 monthly (45,000 credits a month) or $405.00 a year (= $33.75/month, 600,000 credits a year); Pro at 1.5 million credits (internal name "Advanced") $110.00 monthly (112,500 a month) or $990.00 a year (= $82.50/month); Pro at 4 million credits $280.00 monthly (300,000 a month) or $2,520.00 a year (= $210/month). Business: $138.00 a month for 2 seats (45,000 credits per seat per month) or $1,320.00 a year. — [Magnific pricing](https://www.magnific.com/pricing)
- [RD] Page text: "Save 25% with annual"; "Prices exclude VAT and local taxes"; annual plans show "Credits valid for 1 year, no monthly resets"; all three individual plans list "Commercial AI license" (Plus and Pro add "music rights"), "API access with credit-based usage" and "Top up credits anytime". A banner reads "Save 40% on Credits — Seedream 5.5 ... Ends Dec 10. Individual subscriptions only." — [Magnific pricing](https://www.magnific.com/pricing)
- [RD] FAQ text embedded in the page: "If you're on an annual plan, you get all your credits upfront, and they reset every year. If you're on a monthly plan, credits reset every month. Heads up: Unused credits don't roll over to the next month." "We reserve the right to update credit costs at any time, without prior notice." Extra credits can be bought only on Plus or Pro and "expire 3 years after purchase". (The page data also contains an alternative wording in which annual credits are split into 12 monthly allocations; the variant flag served was "control".) — [Magnific pricing](https://www.magnific.com/pricing)
- [RD] Unlimited: Plus and Pro show "UNLIMITED generations" and "Save credits on 30+ models"; the named video model is "Kling 2.5 — All year" (720p; tooltip: "Unlimited Kling 2.5 at 720p is subject to model availability and may change at any time"). Named image models: Nano Banana 2 at 1K (Plus), at 2K (Pro 1.5M), plus Nano Banana Pro (Pro 4M). FAQ: Unlimited "is best for exploring ideas and experimenting freely, although speed may vary"; it "includes priority usage ... Once it runs out, generations run one at a time, and speed varies with demand and volume"; on Plus and Business, Nano Banana Pro (1K/2K), Nano Banana 2 (2K), Flux.2 Flex, Flux.2 Max and GPT Image 1.0 / 1.5 "are moving from Unlimited to credits ... at your next renewal". A tooltip string says full speed lasts "up to 800 gen/mo on Premium+ and 5,000 gen/mo on Pro; after that, generation continues at a slower pace". — [Magnific pricing](https://www.magnific.com/pricing)
- [RD] "Pay safe and cancel anytime. Encrypted transactions, 30-day refund guarantee, no cancellation fees." [SS, vendor help page] The refund applies only within 30 days of payment and only if the service has not been used: "no downloads ... and no AI credits consumed"; annual payments are refunded in full if eligible, never pro rata; extra-credit packs have a separate 14-day window. — [Magnific pricing](https://www.magnific.com/pricing); [Magnific/Freepik subscriptions and refunds](https://www.freepik.com/ai/docs/subscriptions-and-refunds)

**Table 6a. Magnific video and image credit costs.** [RD] — [Magnific pricing](https://www.magnific.com/pricing). The page shows credits for a sample length (for example "Seedance 2.5 720p — 1,760 credits/4s"); its embedded data stores the per-second rate. Dollar columns are my calculation at $0.001 per credit (Premium or Plus, monthly billing) and $0.000675 (Plus, annual billing).

| Model and setting | Credits per second | Page example | 5 s clip, credits | $ monthly billing | $ Plus annual |
|---|---|---|---|---|---|
| Seedance 2.5, 720p | 440 | 1,760 per 4 s | 2,200 | 2.20 | 1.49 |
| Seedance 2.5 Draft, 480p | 200 | 800 per 4 s | 1,000 | 1.00 | 0.68 |
| Seedance 2.5, 1080p | 790 | 3,160 per 4 s | 3,950 | 3.95 | 2.67 |
| Seedance 2 Pro, 720p | 280 | 1,120 per 4 s | 1,400 | 1.40 | 0.95 |
| Seedance 2.0 Fast, 720p | 235 | 940 per 4 s | 1,175 | 1.18 | 0.79 |
| Kling 4.0, 1080p | 280 | 840 per 3 s | 1,400 | 1.40 | 0.95 |
| Kling 3.0 Pro, 1080p | 90 | 450 per 5 s | 450 | 0.45 | 0.30 |
| Kling 2.5, 720p (unlimited on Plus, Pro, Business) | 28 | 140 per 5 s | 140 | 0.14 | 0 on Plus |
| MiniMax H3 Max, 768p | 80 | 400 per 5 s | 400 | 0.40 | 0.27 |
| MiniMax H3 Max Turbo, 768p | 40 | 200 per 5 s | 200 | 0.20 | 0.14 |
| MiniMax H3, 2K | 110 | 550 per 5 s | 550 | 0.55 | 0.37 |
| Wan 3.0, 720p | 100 | 200 per 2 s | 500 | 0.50 | 0.34 |
| Wan 3.0 Prime, 1080p | 340 | 680 per 2 s | 1,700 | 1.70 | 1.15 |
| Gemini Omni 1.1 | 240 | 720 per 3 s | 1,200 | 1.20 | 0.81 |
| Veo 3.1, 4K with audio | 520 | 2,080 per 4 s | 2,600 | 2.60 | 1.76 |

- [RD] Image credits per image: Nano Banana 2.1 at 2K 65; Nano Banana Pro at 1K/2K 75 (4K 150); Nano Banana 2 at 1K or 2K 75; Nano Banana 2 Lite at 1K 60; Seedream 5.0 Pro at 2K 75; GPT 2.6 Medium at 2K 65; Flux.2 Pro at 1K 50; Magnific One High at 2K 180. At $0.001 per credit these are $0.05-$0.18 per image. — [Magnific pricing](https://www.magnific.com/pricing)
- [SS] Trustpilot shows Magnific at 3.8 from about 2,971 reviews in one snapshot and 4.0 from more than 3,100 in another (the legacy Freepik page shows 2 of 5); complaints include unlimited access removed or slowed under fair-use rules, a year-long Unlimited plan losing benefits after a few months, credits draining quickly (the video upscaler is named) and unresolved refund requests. — [Trustpilot, Magnific](https://uk.trustpilot.com/review/magnific.ai?page=4); [eesel review, third party](https://www.eesel.ai/blog/freepik-ai-reviews)

**Artlist**
- [RD] AI plans on the pricing page (toggle "Monthly / Yearly — Save 40%"): AI Starter $19.99 monthly or $11.99/month "billed annually", 16,500 credits, "up to 1,650 AI images / up to 103 AI videos", "includes up to 3 members"; AI Core ("Most Popular") $39.99 or $23.99, 40,000 credits, "up to 250 AI videos", with "Unlimited Generations" on some models plus monthly fast generations and parallel generations; AI Pro $99.99 or $59.99, 120,000 credits, "up to 750 AI videos". Every card says "License covers commercial use". "Prices exclude VAT and local taxes, calculated at checkout." — [Artlist pricing](https://artlist.io/page/pricing/max)
- [RD, vendor blog dated 5 Nov 2026] "AI Starter with 16,500 credits, AI Core with 40,000 and AI Creator with 80,000": billed annually $11.99 / $23.99 / $41.67 per month (annual totals $143.88 / $287.88 / $499.99); billed monthly $19.99 / $39.99 / $69.99. Unlimited models: none / 8 / 18. Fast generations: none / 700 / 900 a month. Parallel generations: none / 4 / 5. "Unlimited needs a yearly plan from 40,000 credits, so monthly plans and AI Starter do not include it." "Artlist MCP usage is credit-based." — [Artlist AI pricing blog](https://artlist.io/blog/ai-tools-pricing-plans/)
- [RD] Unlimited models on AI Core (8): Nano Banana 2 Lite (1K), Meta Muse Image (2K), Seedream 5.0 Pro, Nano Banana 2.1 (1K, web search off), and four video models: Gemini Omni 1.1 Flash (360p, up to 5 s, with audio), Wan 3.0 (480p, up to 5 s, with audio), Seedance 2.0 Mini (480p, up to 5 s, with audio), MiniMax H3 Max (480p, 5 s). AI Creator adds 10: Nano Banana 2 (2K), GPT Image 2 (low and medium), Z-Image Turbo (2K), Artlist Original 1.0, Nano Banana, GPT Image 1.5, Veo 3.1 Lite (720p, 4 s), Seedance 1.0 Pro Fast (1080p, 5 s, no audio), Kling 2.5 Turbo Pro (1080p, 5 s, no audio), LTX 2.3 Pro (1080p, 6 s, no audio). "The model list changes often." — [Artlist AI pricing blog](https://artlist.io/blog/ai-tools-pricing-plans/)
- [RD] Unlimited fine print: "Unlimited applies only to supported models and is subject to plan features, model availability, technical capacity, and reasonable use limitations." "You get a set number of fast generations each month. Once those are used, you still have unlimited access — generations simply process at a standard speed." "Unlimited is for human use only ... we don't permit automation, scraping or account sharing." Page data adds "provided reasonable use limits, daily thresholds, or misuse restrictions apply" and "unused Fast generations don't roll over". A banner string reads "Coming soon: Seedance 2.5 Unlimited for a year". — [Artlist pricing](https://artlist.io/page/pricing/max)
- [RD] "Your credits renew every month"; "Can I try Artlist for free? Yes! You can generate free voiceovers, images, a video, and music". Max Business: up to 7 members at $399.00 a month billed annually, 180,000 credits, 900 fast generations, Unlimited on 24 models. — [Artlist pricing](https://artlist.io/page/pricing/max); [Artlist AI pricing blog](https://artlist.io/blog/ai-tools-pricing-plans/)
- [RD, vendor blog dated 14 May 2026] After a credit cut across 46 model variants, credits per unit are: Kling 3.0 Pro 100 without audio, 150 with; Kling 3.0 Standard 80 / 120; Kling O3 Standard 80 / 100; Kling 2.6 Pro 80 / 150; Veo 3.1 Lite 720p 63 / 94 and 1080p 100 / 125; Veo 3.1 250 / 425; Veo 3.1 Fast 125 / 200; Seedance 2.0 200 (480p), 300 (720p), 600 (1080p); Seedance 2.0 Fast 120 (480p), 300 (720p); images: Nano Banana 40, Nano Banana 2 at 1K 90, Nano Banana Pro at 1K/2K 160. The table does not state the unit; the first round's help-centre source says these are per second of video. — [Artlist credits reduction](https://artlist.io/blog/artlist-credits-reduction/)
- [SS, vendor help centre] Seedance 2.5 with audio is listed at roughly 200 credits per second at 480p, 500 at 720p and 1,000 at 1080p; Seedance 2.5 Flash 200 (480p) and 300 (720p); MiniMax H3 with audio 120 per second at 2K; no rate for Kling 4.0 or MiniMax H3 Max was found. — [Artlist help: credits for AI image and video](https://help.artlist.io/hc/en-us/articles/38815633707421-Artlist-AI-Tools-Understanding-credits-for-AI-Image-and-Video)
- [RD] Artlist's Seedance 2.5 model page says the model offers "480p and 720p at 24 frames per second (FPS) at launch" and points to the pricing page for costs; the Kling 4.0 and MiniMax H3 model pages state no credit costs. — [Artlist Seedance 2.5](https://artlist.io/ai/models/seedance-2-5)
- [SS] Trustpilot shows Artlist at 3.2 from roughly 2,000-2,400 reviews; complaints include credits deducted for unusable outputs, refused refunds and an annual plan whose credits ran out after a few videos; a Cined commentary argues Artlist's terms define "Unlimited" narrowly and advises against buying an annual AI plan. — [Trustpilot, Artlist](https://www.trustpilot.com/review/artlist.io?page=1); [Cined](https://www.cined.com/?p=435652)

**Verdicts on first-round figures**
- CORRECTS (Magnific): the two "snapshots" are one ladder. $20 for Premium is the monthly-billing price (annual is $14.50/month), not the annual rate; Plus is $45 monthly / $33.75 annual; "Pro $110 with 1.5M credits" and "Pro $280 ($210 annual) with 4M credits" are two sizes of the same Pro plan; Business is $138 for 2 seats ($69 per seat) as reported.
- NEW (Magnific): per-video credit costs (first-round gap). The single first-round figure "Hailuo 2.3 Fast 768p = 150 credits per 6 s" does not appear on the current page. Higgsfield's claim that a 10-second 720p Seedance 2.5 clip costs 4,400 credits on Magnific matches (440 per second).
- CONFIRMS (Magnific): about $0.001 per credit; unlimited list being narrowed at renewal on Plus and Business.
- CONFIRMS (Artlist): all three plan prices and credit amounts; Max Business; Unlimited needing a yearly plan of 40,000+ credits with 8 and 18 models; Veo 3.1 at 250, Veo 3.1 Fast at 125, Veo 3.1 Lite 720p at 63 and Kling 3.0 Pro without audio at 100 credits per second (same numbers in Artlist's own May 2026 table).
- NEW (Artlist): the Unlimited lists by model and setting, the fast-generation quotas (700 on AI Core, 900 on AI Creator) and the parallel limits (4 and 5), which the first round could not find. The live page now shows a 120,000-credit "AI Pro" card at $99.99 / $59.99 in the third position; the 80,000-credit AI Creator appears in the 5 November blog.

### Inferences
- Magnific's credit prices track API list prices almost exactly at $0.001 per credit: MiniMax H3 Max 768p is $0.08 per second (the same as fal's standard rate), Wan 3.0 720p $0.10 (same as fal), Kling 3.0 Pro 1080p $0.09 (below fal's $0.112), Seedance 2.5 720p $0.44 (below fal's $0.473, above kie.ai's $0.315), Kling 4.0 1080p $0.28 (above fal's $0.235). Monthly Magnific is therefore roughly "API pricing plus stock library, editor and upscaler"; only annual billing (27-33% cheaper per credit) undercuts fal.
- Artlist per-generation cost (my calculation; $ per credit is $0.00121 / $0.00100 / $0.000875 on monthly billing and $0.000727 / $0.00060 / $0.000521 on annual billing for Starter / Core / Creator): Kling 3.0 Pro 1080p, 5 s without audio (500 credits) costs $0.61 / $0.50 / $0.44 monthly and $0.36 / $0.30 / $0.26 annual; Seedance 2.5 720p, 5 s (2,500 credits, search-summary rate) costs $3.03 / $2.50 / $2.19 monthly and $1.82 / $1.50 / $1.30 annual; Veo 3.1 Lite 720p, 8 s without audio (504 credits) costs $0.61 / $0.50 / $0.44 monthly and $0.37 / $0.30 / $0.26 annual.
- Artlist AI Core on yearly billing ($287.88 paid up front) is the only standing offer found that gives credit-free generation on a model in Artificial Analysis's current top ten (MiniMax H3 Max), but capped at 480p and 5 seconds, with 700 fast generations a month and "standard speed" afterwards. For 9:16 social video 480p means an upscaling step; whether the result holds up was not tested.
- Artlist's card claim "up to 103 AI videos" from 16,500 credits implies 160 credits per video, i.e. a 2-second clip on an 80-credit-per-second model or similar; like Krea's headline counts it is not a realistic count of 5-second clips on a current model.

### Gaps
- Magnific's help pages (unlimited models list, refunds) returned HTTP 403; the full list of the "30+" unlimited models and the fast-generation quota in force were not confirmed. Whether monthly-billed credits are 20,000 a month (as the price data says) with no carry-over was read from an embedded FAQ string, not from a rendered page.
- Artlist credit costs for Kling 4.0 and MiniMax H3 Max, and the current per-second table, could not be read directly (help centre is a blocked host). The Seedance 2.5 rates are from a search summary.
- Artlist's refund and cancellation terms were not read.
- The complaint evidence for both platforms is from search summaries of Trustpilot pages.

---

## 7. Conclusion: cheapest reliable route to 20-60 image-to-video clips of 5-8 seconds a month, (a) frontier model and (b) near-frontier budget model; pay-as-you-go versus subscription; monthly versus annual

### Takeaway
For a near-frontier budget model the cheapest reliable route is a prepaid pay-as-you-go balance on fal.ai using MiniMax H3 at 768p ($0.06 per second) or HeyGen Video 1 ($0.02 per second): 20-60 usable 5-second clips at 3 generations each cost $18-$54 (MiniMax H3) or $6-$18 (HeyGen Video 1) a month with no subscription and no annual lock-in. For the frontier model (Seedance 2.5) every route is about 3 to 24 times dearer per generation; the cheapest verified one is Krea on yearly billing ($0.90 per 5-second 720p generation, $252-$756 paid up front), the cheapest without commitment is kie.ai pay-as-you-go ($1.58, with reliability caveats) or Krea monthly ($1.50), and fal ($2.31-$2.37) is the dearest; the rational plan is to use the budget model for most shots and buy Seedance 2.5 only for hero shots, drafting at 480p first.

### Cited Findings
(All inputs are figures already cited in sections 1-6; the arithmetic is mine. Assumption used throughout unless stated: **3 generations per usable shot**, so 20-60 usable clips = 60-180 generations = 300-900 generated seconds at 5 s or 480-1,440 seconds at 8 s.)

- [RD] Quality basis: Seedance 2.5 is #1 on AA image-to-video (1161) and #1 in its "Animation & Gaming" category; MiniMax H3 768p is #4 (1134), HeyGen Video 1 #6 (1124), MiniMax H3 Max #9 (1116), Wan 3.0 #11 (1109), Gemini Omni Flash 1.2 #14 (1085), Kling 3.0 Pro #23 (1000), Veo 3.1 Lite #29 (931); Kling 4.0 is unrated. — [AA image-to-video leaderboard](https://artificialanalysis.ai/video/leaderboard/image-to-video)
- [RD] Pay-as-you-go rates per second used below: Seedance 2.5 720p $0.4730 on fal and $0.315 on kie.ai; Seedance 2.5 480p $0.2205 and $0.14; MiniMax H3 768p $0.06 and $0.04; HeyGen Video 1 at 768p $0.02 on fal (regular price); MiniMax H3 Max 768p $0.08 on fal; Kling 4.0 720p $0.157 and $0.1425. — [fal Seedance 2.5](https://fal.ai/models/bytedance/seedance-2.5/image-to-video); [kie.ai Seedance 2.5](https://kie.ai/seedance-2-5); [fal MiniMax H3](https://fal.ai/models/minimax/h3/image-to-video); [kie.ai MiniMax H3](https://kie.ai/minimax-h3); [fal HeyGen Video](https://fal.ai/models/heygen/heygen-video/image-to-video); [fal H3 Max](https://fal.ai/models/minimax/h3-max/image-to-video); [fal Kling 4.0](https://fal.ai/models/kling/v4/image-to-video); [kie.ai Kling 4.0](https://kie.ai/kling-4-0)
- [RD] Subscription inputs used below: Krea $0.00175 per unit monthly and $0.00105 yearly, Seedance 2.5 at 856 units (720p, 5 s) and about 380 (480p, 5 s); Higgsfield Plus $49 for 1,000 credits and Ultra $129 ($99 on annual billing) for 3,000, Seedance 2.5 at 35 credits (720p, 5 s); Magnific $0.001 per credit monthly, Seedance 2.5 at 440 credits per second (720p); Artlist AI Core $39.99 monthly or $23.99 annual for 40,000 credits. — [Krea pricing](https://www.krea.ai/pricing); [Krea Seedance 2.5 pricing](https://www.krea.ai/blog/seedance-2-5-pricing-cost-per-video); [Higgsfield pricing explained](https://higgsfield.ai/blog/higgsfield-pricing-explained); [Higgsfield annual unlimited plans](https://higgsfield.ai/blog/annual-unlimited-ai-video-plans); [Magnific pricing](https://www.magnific.com/pricing); [Artlist AI pricing blog](https://artlist.io/blog/ai-tools-pricing-plans/)
- [RD] Terms that bear on "reliable": fal credits expire after 365 days and server errors are not billed; kie.ai credits "never expire" but the service is "as is" with refunds "if needed"; Higgsfield refunds only within 7 days and only if no credit was used; Krea units do not roll over; Magnific "reserve[s] the right to update credit costs at any time, without prior notice". — [fal FAQ](https://fal.ai/docs/documentation/model-apis/faq.md); [kie.ai terms](https://kie.ai/terms-of-use); [Higgsfield Terms of Use](https://higgsfield.ai/terms-of-use-agreement); [Krea pricing](https://www.krea.ai/pricing); [Magnific pricing](https://www.magnific.com/pricing)
- [SS] Reputation signals: kie.ai about 2.1 of 5 from 16 Trustpilot reviews and no status page; fal 2.4-2.9 from 4-17 reviews; Krea 2.5-3.6 from 74-183; Artlist 3.2 from about 2,000-2,400; Magnific 3.8-4.0 from about 3,000; Higgsfield 4.0 from about 5,500 with about 19% one-star. — [gengrades on kie.ai](https://gengrades.com/kie-ai); [Trustpilot, fal.ai](https://ca.trustpilot.com/review/fal.ai); [Trustpilot, Krea](https://uk.trustpilot.com/review/krea.ai); [Trustpilot, Artlist](https://www.trustpilot.com/review/artlist.io?page=1); [Trustpilot, Magnific](https://uk.trustpilot.com/review/magnific.ai?page=4); [Trustpilot, Higgsfield AI](https://www.trustpilot.com/review/higgsfield.ai)

### Inferences

**(b) Near-frontier budget model: pay-as-you-go wins**

Table 7a. Monthly cost of 60 and 180 generations (20 and 60 usable clips at 3 generations each). My calculation: seconds x rate.

| Model, resolution (AA image-to-video rank) | Where | $ per second | One 5 s / 8 s generation | 60 / 180 generations of 5 s | 60 / 180 generations of 8 s |
|---|---|---|---|---|---|
| HeyGen Video 1, 768p (#6) | fal | 0.02 | $0.10 / $0.16 | $6 / $18 | $9.60 / $28.80 |
| MiniMax H3, 768p (#4) | kie.ai | 0.04 | $0.20 / $0.32 | $12 / $36 | $19.20 / $57.60 |
| MiniMax H3, 768p (#4) | fal | 0.06 | $0.30 / $0.48 | $18 / $54 | $28.80 / $86.40 |
| MiniMax H3 Max Turbo, 768p | fal | 0.04 | $0.20 / $0.32 | $12 / $36 | $19.20 / $57.60 |
| MiniMax H3 Max, 768p (#9) | fal | 0.08 | $0.40 / $0.64 | $24 / $72 | $38.40 / $115.20 |
| Gemini Omni Flash 1.2, 720p (#14) | kie.ai / fal | 0.045 / 0.0819 | $0.23 / $0.41 (5 s) | $13.50 / $40.50; $24.57 / $73.71 | $21.60 / $64.80; $39.31 / $117.94 |
| Wan 3.0, 720p (#11) | kie.ai / fal | 0.08 / 0.10 | $0.40 / $0.50 (5 s) | $24 / $72; $30 / $90 | $38.40 / $115.20; $48 / $144 |
| Veo 3.1 Lite, 720p with audio (#29) | fal | 0.05 | $0.25 / $0.40 | $15 / $45 | $24 / $72 |
| Kling 3.0 Standard, 720p silent (Standard tier unrated; Kling 3.0 Pro is #23) | kie.ai / fal | 0.0755 / 0.084 | $0.38 / $0.42 (5 s) | $22.65 / $67.95; $25.20 / $75.60 | $36.24 / $108.72; $40.32 / $120.96 |
| Kling 4.0, 720p (unrated) | kie.ai / fal | 0.1425 / 0.157 | $0.71 / $0.79 (5 s) | $42.75 / $128.25; $47.10 / $141.30 | $68.40 / $205.20; $75.36 / $226.08 |

- Recommended budget route: fal.ai prepaid balance, MiniMax H3 at 768p as the default and HeyGen Video 1 as the cheapest alternative. Monthly cost $18-$54 (MiniMax H3) or $6-$18 (HeyGen Video 1) for 5-second clips, $29-$86 or $10-$29 for 8-second clips. Reasons: both are in AA's top six for image-to-video, within 27-37 Elo of the leader; fal publishes exact per-second prices, bills only successful outputs, and has a form-based playground; no subscription, no annual prepayment, and unused credit lasts 365 days.
- kie.ai would lower MiniMax H3 to $12-$36 a month, a saving of $6-$18. That is too small to justify the weaker reliability record and opaque sourcing; it is a reasonable second account for experiments, funded with a $5 pack.
- Subscriptions do not beat this at 20-60 clips. Magnific Premium on monthly billing ($20, 20,000 credits) yields 50 MiniMax H3 Max 768p generations of 5 s ($0.40 each, the same per-second price as fal) or 100 H3 Max Turbo generations; it is worth it only for the stock library, editor and upscaler. Krea Basic ($9 monthly, 5,000 units) yields 38 MiniMax H3 Max generations but at 480p; Krea Pro ($35, or $21 yearly) yields 153 at 480p. Artlist AI Core on yearly billing ($287.88 up front, $23.99 a month) gives credit-free MiniMax H3 Max and Wan 3.0 at 480p and 5 s plus 40,000 credits (80 Kling 3.0 Pro 1080p clips): attractive on paper, but 480p-only for the unlimited part and a 12-month prepayment. Higgsfield Starter ($15, 200 credits) yields about 20 Kling 3.0 720p generations ($0.75 each) and no access to the top models.

**(a) Frontier model (Seedance 2.5 at 720p)**

Table 7b. Cost of one 5-second 720p Seedance 2.5 generation, cheapest first. My calculation from the cited rates.

| Route | Billing | $ per generation | What must be paid up front | Generations per month included |
|---|---|---|---|---|
| Krea Pro / Max | yearly | 0.90 | $252 (Pro), $504 (Max 40k), $756 (Max 60k) | 23 / 46 / 70 |
| Higgsfield Ultra | annual ($99/month, per a September post) | 1.16 | $1,188 | 85 |
| Artlist AI Creator / AI Core | annual | 1.30 / 1.50 (credit rate from a search summary) | $499.99 / $287.88 | 32 / 16 |
| Magnific Plus / Premium | annual | 1.49 / 1.59 | $405 / $174 | 22 / 9 |
| Krea Pro / Max | monthly | 1.50 | $35 / $70 / $105 | 23 / 46 / 70 |
| Higgsfield Ultra | monthly | 1.50 | $129 | 85 |
| kie.ai | pay as you go | 1.58 | $5 minimum pack | any |
| Higgsfield Plus | monthly | 1.72 | $49 | 28 |
| Magnific Premium / Plus | monthly | 2.20 | $20 / $45 | 9 / 20 |
| fal.ai | pay as you go | 2.31-2.37 | not stated | any |
| Artlist AI Core / Starter | monthly | 2.50 / 3.03 (search-summary rate) | $39.99 / $19.99 | 16 / 6 |

- If every one of the 3 generations per usable clip is made at 720p, the monthly bill for 20 / 60 usable 5-second clips (60 / 180 generations) is: kie.ai $94.50 / $283.50; fal $141.90 / $425.70; Krea 51,360 / 154,080 units, i.e. Max 60k for 20 clips ($105 monthly, or $63 a month on yearly billing = $756 up front) and more than the largest self-serve size shown for 60 clips; Higgsfield 2,100 / 6,300 credits, i.e. Ultra at $129 for 20 clips and Ultra at the 6,000-credit setting (reported at $250) plus a pack for 60 clips. For 8-second clips multiply by 1.6 (kie.ai $151 / $454; fal $227 / $681).
- A cheaper frontier workflow uses the model's own low-resolution draft: 2 drafts at 480p plus 1 final at 720p per usable 5-second clip. Per usable clip that is $2.98 on kie.ai (2 x $0.70 + $1.575), $4.57 on fal (2 x $1.10 + $2.365), 1,616 Krea units ($2.83 monthly billing, $1.70 yearly), about 65 Higgsfield credits ($3.19 on Plus, $2.80 on Ultra monthly, $2.15 on Ultra annual; the 15-credit figure for a 5-second 480p draft is scaled from 30 credits per 10 seconds) and 4,200 Magnific credits ($4.20 monthly, $2.84 on Plus annual). For 20 / 60 usable clips: kie.ai $59.50 / $178.50; fal $91.40 / $274.20; Krea 32,320 / 96,960 units (Max 40k at $70 monthly or $42 yearly covers 24 clips; 60 clips need about 100,000 units, whose price was not shown; at the flat per-unit rate it would be about $175 monthly or $105 yearly); Higgsfield 1,300 / 3,900 credits (Ultra, $129, covers 46 clips).
- Cheapest reliable frontier route by commitment level: (1) with annual prepayment, Krea Max 40k on yearly billing: $504 up front ($42 a month) for 24 usable clips a month with drafts, $1.70 per usable clip; (2) month to month on a subscription, Krea Max 40k at $70 (24 usable clips, $2.83 each) or Krea Pro at $35 (12 usable clips); (3) pure pay-as-you-go, kie.ai at $2.98 per usable clip if its reliability risk is accepted, otherwise fal at $4.57. Higgsfield Ultra is competitive on price per clip ($2.15-$2.80) but needs $129 a month and carries the weakest refund terms.
- Seedance 2.0 is a cheaper stand-in for "frontier": it is #3 overall on AA image-to-video (1141) and statistically level with 2.5 in the "Animation & Gaming" and "Social Media & Creator Content" categories, and it costs $0.3024 per second on fal and $0.205 on kie.ai at 720p (36% and 35% less than Seedance 2.5), or 30 Higgsfield credits per 5 seconds against 35.

**Pay-as-you-go versus subscription, monthly versus annual**
- At this volume a budget model on pay-as-you-go ($6-$54 a month) costs less than any subscription that would cover the same work, and has no expiry pressure (fal: 365 days; kie.ai: none) and no renewal. Subscriptions add editors, stock assets and project libraries but, on monthly billing, charge the same or more per second for the same models (Magnific $0.08 per second for MiniMax H3 Max 768p, identical to fal).
- For Seedance 2.5 the picture reverses relative to fal: Krea (either billing), Higgsfield (Plus or Ultra) and Magnific's annual plans all undercut fal's $2.31-$2.37 per generation, by about 26% (Higgsfield Plus, $1.72) to 62% (Krea yearly, $0.90), and Krea monthly ($1.50) matches kie.ai ($1.58). So a subscription is the cheaper route to the frontier model for anyone unwilling to rely on kie.ai.
- Annual prepayment lowers the per-credit price by 40% at Krea and Artlist, 25-27% at Magnific and 23% on Higgsfield Ultra. It pays off only if the plan is used for at least about 7.2 months of the 12 at Krea Pro or Artlist AI Core ($252 / $35 and $287.88 / $39.99), 8.7 months at Magnific Premium ($174 / $20) and 9.2 months at Higgsfield Ultra ($1,188 / $129). Against that: the #1 model has changed several times in 2026 (first round), vendors can change credit costs or unlimited lists mid-term (Magnific says so explicitly; Higgsfield and Artlist reserve fair-use throttling), units do not roll over, and refunds are lost once any credit is used (Higgsfield 7 days, Magnific 30 days). For a creator who is still choosing a model, monthly billing or pay-as-you-go is the safer default; an annual Krea plan is defensible only after a month of real use shows Seedance 2.5 is needed regularly.
- Illustrative mixed plan on one fal balance (my calculation): 20 usable 5-second clips a month, of which 16 are made on MiniMax H3 768p with 3 generations each (48 x $0.30 = $14.40) and 4 hero shots on Seedance 2.5 with two 480p drafts and one 720p final (4 x $4.57 = $18.28): about $33 a month. Replacing the hero shots with Krea Pro monthly ($35 for up to 12 such shots) would cost more in total at this volume.

**Sensitivity**
- If 5 generations are needed per usable clip instead of 3 (Higgsfield's own planning range is "three to five attempts"), multiply every pay-as-you-go total by 1.67; subscriptions then run out of credits sooner (Krea Pro: 4 usable 720p Seedance clips instead of 7).
- At 1080p Seedance 2.5 costs 2.46 times the 720p rate on fal and 2.5 times on kie.ai and Krea; generating at 720p and upscaling is the obvious economy, but the upscaling step was not priced.
- Image step: a start frame costs about $0.04 (Nano Banana 2.1 at 1K on fal), $0.02 on kie.ai, $0.03 (Seedream 5.5) or $0.15 (Nano Banana Pro); even 3 images per clip for 60 clips is $3.60-$27 a month and does not change the ranking.

### Gaps
- No verified price for Seedance 2.5 on ByteDance's own channels was read in this task (AA's maker-API figure of $0.569 per second at 1080p suggests the maker's price is about half of fal's); first-party subscriptions such as Dreamina, Kling, Hailuo and Google are covered by other researchers and may undercut every route above.
- The actual share of usable generations for stylised 3D prompts on each model is unknown; 3 per usable shot is an assumption.
- HeyGen Video 1's current fal price depends on whether the expired 50% promotion text on the page still applies; Higgsfield's live plan prices and Krea's 80k / 100k Max prices were not readable; Artlist's Seedance 2.5 rate is from a search summary.
- Minimum top-up and any sign-up bonus on fal are unverified, so the smallest practical first purchase there is not known.
- VAT is excluded everywhere; an EU buyer should expect roughly 20% more on subscriptions that state "prices exclude VAT" (Magnific, Artlist), and should check how fal and kie.ai handle tax at checkout.
- Reliability evidence for all six services rests on search summaries of review sites with small or self-selected samples; no uptime measurements were found.
