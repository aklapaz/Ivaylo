# First-party AI video generators from US/Europe-based vendors: fact sheet as of 17 November 2026

> **Read this first: research limits.**
> 1. Direct page fetches were blocked for every site tried (the session's network policy allows no external hosts), so no vendor page could be opened and read in full.
> 2. The shared web-search budget ran out after 15 searches. Eight further searches (Google Omni details, Flow free tier and Whisk, Veo API status, xAI docs, the X Subscription, Runway free plan, Luma Ray3.2, Pika) returned nothing.
> 3. Result: Google, OpenAI, Runway and Luma are reasonably covered. xAI and Midjourney are partial and rest mostly on third-party sources. **Pika, Adobe Firefly, Meta, Lightricks/LTX Studio, Moonvalley, 2026 newcomers and the "3D look" quality question have no verified findings.**
> 4. Figures labelled "official" come from the search tool's summaries of the vendor's own pages, not from reading the pages directly. Re-check them on the live pages before publishing.
>
> **Evidence labels:** [OFF] = the vendor's own page, read through a search summary. [3P] = third-party blog, guide or press. [SOC] = post on X. Dates decoded from X post IDs are my own calculation.
>
> **Attribution caveat:** each search returned one summary covering about ten pages. Where a third-party claim could have come from more than one of those pages, I link the most likely one or two. The claim was in the result set, but the exact page may differ. Most pages showed no publication date; I give a date only where the result stated one.
>
> **Costing assumption used throughout:** one finished 30-second video = 4 shots, with 3 generations per usable shot = 12 generations. I cost it as 12 clips of 8 seconds (96 generated seconds) unless stated. Credit value = plan price divided by monthly credits. This ignores free daily credits, unused credits, tax, upscaling and any editing or audio tools.

## 1. Flagship model, modes and specs per vendor

### Takeaway
Google's line-up changed in 2026: Gemini Omni Flash (version 1.2, 5 November 2026) is now the default video model in the Gemini app and sits beside Veo 3.1 Lite in Flow, while Veo 3.1 Fast and Quality leave Flow on 5 December 2026. OpenAI no longer sells any video generator (Sora app closed 26 April 2026, API closed 24 September 2026); Runway's priced flagship is Gen-4.5 and Luma's is Ray3.2. Specs for the other vendors could not be verified.

### Cited Findings

#### Google (Veo family, Gemini Omni Flash, Flow, Gemini app, API)
- [OFF] Flow prices these video models: Omni Flash 1.2 and Veo 3.1 Lite (current), plus Veo 3.1 Fast, Veo 3.1 Quality and Omni Flash 1.1 (listed as older models). Page undated; it reflects the November 2026 line-up. — [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- [OFF] Veo 3.1 Fast, Veo 3.1 Quality and Omni Flash 1.1 will be retired from Flow on 5 December 2026. Google recommends moving to Omni Flash 1.2 or Veo 3.1 Lite. — [Flow Help: models and supported features](https://support.google.com/flow/answer/16352836?hl=en)
- [OFF] Omni Flash 1.2 in Flow generates or edits video up to 15 seconds, at 360p or 720p (priced per second). — [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en); [Gemini subscriptions page](https://gemini.google/subscriptions/)
- [OFF] Veo 3.1 Lite in Flow makes 4, 6 or 8 second clips at 720p. Veo 3.1 Quality makes 8 second clips. — [Flow Help: Manage your Google Flow credits (Android view)](https://support.google.com/flow/answer/16526234?hl=en&co=GENIE.Platform%3DAndroid)
- [OFF] Google's plan comparison table lists Omni Flash as the video generation model for Google AI Plus, Pro and Ultra. — [Gemini subscriptions page](https://gemini.google/subscriptions/)
- [3P] Omni Flash has replaced Veo 3.1 as the default video model in the Gemini app for paying subscribers; Veo 3.1 still exists outside the consumer app. One guide attributes this to Google's own product FAQ. — [BuildFastWithAI review](https://www.buildfastwithai.com/blogs/gemini-omni-flash-review-google-ai-video-model-2026); [GeoToolbox guide](https://geotoolbox.ai/blog/gemini-omni)
- [3P] At launch Omni Flash produced 10-second clips with synchronized audio, carried a SynthID watermark, and shipped without audio editing. — [WaveSpeed: "Gemini Omni Flash Shipped"](https://wavespeed.ai/blog/posts/gemini-omni-flash-shipped-what-actually-launched/)
- [3P] Omni Flash 1.2 was released on 5 November 2026, raised clip length to 15 seconds and doubled paid-tier API rate limits. — [Apidog: Gemini Omni 1.2 Flash or Veo](https://apidog.com/blog/gemini-omni-1-2-flash-or-veo/)
- [3P] After version 1.1, scene extension stretches an Omni Flash video to 40 seconds in 10-second steps (one guide in the result set; exact page not confirmed). — [invideo guide](https://invideo.io/blog/gemini-omni-flash-guide/); [GeoToolbox guide](https://geotoolbox.ai/blog/gemini-omni)
- [3P] Omni Flash is described as a "talk-to-edit" model: video is edited by conversation, and it is available through the API. — [Fello AI](https://felloai.com/gemini-omni-flash/); [VentureBeat](https://venturebeat.com/technology/googles-gemini-omni-flash-hits-the-api-turning-enterprise-video-production-into-a-conversation)
- [3P, conflicting] Resolution: one source says Omni Flash only generates 720p; another says it upscales to 1080p or 4K, so 720p is a generation limit and not a delivery limit. — [BuildFastWithAI review](https://www.buildfastwithai.com/blogs/gemini-omni-flash-review-google-ai-video-model-2026); [Coursiv guide](https://coursiv.io/blog/gemini-omni-flash)
- [OFF] The Gemini API price list still shows Veo 3.1 Lite, Fast and Standard, all with audio: Lite at 720p and 1080p (no 4K); Fast and Standard at 720p, 1080p and 4K. — [Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing?hl=en)
- [3P, conflicts with the line above] One guide says Veo can no longer be called from the Gemini API because its Preview models were shut down on 22 October 2026. — [Apidog: Gemini Omni 1.2 Flash or Veo](https://apidog.com/blog/gemini-omni-1-2-flash-or-veo/)
- [OFF, title only] Google Cloud announced Veo 3.1 Lite and a new Veo upscaling capability on Vertex AI. — [Google Cloud blog](https://cloud.google.com/blog/products/ai-machine-learning/veo-3-1-lite-and-a-new-veo-upscaling-capability-on-vertex-ai)
- [OFF, title only] Google Cloud's pricing page for these models is now titled "Agent Platform Pricing" (Gemini Enterprise Agent Platform), which appears to be the current name for what was Vertex AI. — [Google Cloud pricing page](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing)

#### OpenAI (Sora)
- [OFF] The Sora web and app experiences were discontinued on 26 April 2026. The Sora API end date is 24 September 2026. — [OpenAI Help: What to know about the Sora discontinuation](https://help.openai.com/en/articles/20001152-what-to-know-about-the-sora-discontinuation)
- [OFF] Users were told to export their data (sora.chatgpt.com/sunset) before the API shutdown; remaining content is permanently deleted afterwards. — [OpenAI Help: What to know about the Sora discontinuation](https://help.openai.com/en/articles/20001152-what-to-know-about-the-sora-discontinuation)
- [3P] OpenAI announced the discontinuation on X on 24 March 2026, covering both the mobile app and the API. The Disney licensing partnership tied to Sora was also ending. — [Wikipedia: Sora](https://en.wikipedia.org/wiki/Sora_%28text-to-video_model%29)
- [3P] The Sora Videos API and all sora-2 model variants were switched off on 24 September 2026, with no replacement on the developer roadmap. — [Pondero](https://pondero.ai/news/2026-09-24-openai-sora-api-shutdown/); [AI Watch](https://ai-watch-blog.vercel.app/en/posts/2026-09-24-sora-api-shutdown-effective/)
- [3P] As of October 2026 OpenAI offers no video generator and has not announced a successor. ChatGPT has no built-in video generation. — [Scenema](https://scenema.ai/articles/does-openai-have-a-video-generator); [Kompozy](https://kompozy.io/guides/can-chatgpt-make-videos)
- [3P, rumor] A successor model referred to as "Spud" has been mentioned, with no official confirmation and no consumer product. — [MindStudio](https://www.mindstudio.ai/blog/openai-shutting-down-sora-what-happened)
- [3P, outlier] One source claims Sora 2 generation remains available inside ChatGPT's paid plans. This contradicts the OpenAI help page and the other sources. — [Atlas Cloud](https://www.atlascloud.ai/blog/tips/can-chatgpt-make-videos)

#### Runway
- [OFF] Gen-4.5 is the model Runway prices at the top rate (12 credits per second) and documents in its help center. — [Runway Help: How do credits work?](https://help.runwayml.com/hc/en-us/articles/15124877443219-How-do-credits-work); [Runway Help: Creating with Gen-4.5](https://help.runwayml.com/hc/en-us/articles/46974685288467-Creating-with-Gen-4-5)
- [OFF] The API offers a Gen-4.5 text-to-video endpoint with a 2-second minimum per generation. — [Runway API pricing](https://dev.runwayml.com/pricing)
- [OFF] ProRes or PNG-sequence export is available on Max, Unlimited (Legacy) and Enterprise plans. — [Runway Help: Creating with Gen-4.5](https://help.runwayml.com/hc/en-us/articles/46974685288467-Creating-with-Gen-4-5)
- [3P] Gen-4.5 needs a Standard plan or higher; the Free plan does not include every paid model. — [Magic Hour: Runway Gen-4.5 pricing](https://magichour.ai/blog/runway-gen-45-pricing)

#### Luma (Dream Machine / Ray)
- [OFF] The current video model is Ray3.2; the pricing page also lists Ray3.14. — [Luma pricing](https://lumalabs.ai/pricing)
- [OFF] Ray3.2 text-to-video is offered at 360p (draft), 540p, 720p and 1080p. Video editing (video-to-video) is a separate, more expensive mode. — [Luma Agents docs: pricing](https://docs.agents.lumalabs.ai/guides/pricing/)
- [OFF] Luma's product is now presented as the "Luma Agents" app, with its own FAQ. — [Luma: FAQ about the new Luma Agents app](https://lumalabs.ai/learning-hub/frequently-asked-questions-about-the-new-luma-agents-app)
- [OFF, vendor marketing, title only] Luma promotes a video-to-video restyle that turns real footage into cartoon. — [Luma: restyle real to cartoon](https://lumalabs.ai/video-to-video/restyle-scene-from-real-to-cartoon)
- [3P] Ray 3.14 was released in January 2026 with 1080p output. "Dream Machine" is described as an older, deprecated name replaced by Ray. — [Magic Hour: Luma AI pricing](https://magichour.ai/blog/luma-dream-machine-pricing); [eesel: Luma AI pricing](https://eesel.ai/blog/luma-ai-pricing)

#### Midjourney (video)
- [3P] Midjourney's V8 image model arrived in alpha on 17 March 2026, and V8.2 was the default model as of September 2026. No source gave a video rate or video model specific to V8. — [WaveSpeed: What is Midjourney V8](https://wavespeed.ai/blog/posts/what-is-midjourney-v8-features-pricing-how-to-use-2026); [Tapbit, 9 Sep 2026](https://www.tapbit.com/en/learn/article/midjourney-pricing-features-2026-20260909)
- [3P] Video is generated in SD or HD, by default in batches of four clips; the batch can be cut to one clip to save GPU time. — [Hooked: Midjourney pricing and real cost per video](https://www.hooked.so/compare/midjourney-pricing); [eesel: Midjourney pricing](https://eesel.ai/blog/midjourney-pricing)

#### xAI (Grok Imagine)
- [3P] Grok Imagine video supports text-to-video and up to 1080p; the plan page is reported to list 1080p, 15-second videos from the Super tier ($100). — [AI Business Weekly: Grok Imagine Video](https://aibusinessweekly.net/p/grok-video-generation); [Fello AI: Grok pricing](https://felloai.com/grok-pricing/)
- [3P] The API sells video at 480p, 720p and 1080p. — [BuildFastWithAI: SuperGrok video and image generation](https://blog.buildfastwithai.com/supergrok-video-image-generation-2026-speed-pricing-math-comparison)

#### Lightricks, Adobe, Pika, Meta, Moonvalley
- [3P, title only] A 2026 independent review tests "LTX-2.3", which suggests that is Lightricks' current model generation. — [DEV Community review](https://dev.to/hoelee/best-ai-video-generators-in-2026-free-vs-paid-and-my-ltx-23-test-3clf)
- [3P] Round-ups recommend Adobe Firefly for commercially safe output and Runway for creative control and editing. — [Pixflow round-up](https://pixflow.net/blog/best-ai-video-generator/); [TechJournal round-up](https://techjournal.org/best-ai-video-generators)

### Inferences
- A creator starting now on Google should build on Omni Flash 1.2 and Veo 3.1 Lite. Veo 3.1 Fast and Quality disappear from Flow in under three weeks (5 December 2026).
- Both surviving Flow models are listed at 720p maximum. Full HD delivery from Flow would rely on upscaling, whose availability and cost I could not confirm.
- OpenAI is not an option. Any workflow, tutorial or price list that mentions Sora is out of date.
- The Gemini API price page and the third-party claim that Veo was removed from the Gemini API on 22 October 2026 cannot both be fully right. A plausible reading is that only preview model IDs were retired, but I could not confirm this.
- Status table (verified data only):

| Vendor | Status, Nov 2026 | Flagship seen in sources | Longest clip / top resolution seen | Native audio seen | Evidence |
|---|---|---|---|---|---|
| Google | Active | Omni Flash 1.2 (5 Nov 2026) and Veo 3.1 Lite; Veo 3.1 Fast/Quality leave Flow 5 Dec 2026 | Omni: 15 s, 720p in Flow. Veo 3.1 Lite: 8 s, 720p in Flow, 1080p by API | Yes (Veo 3.1 priced "with audio"; Omni "synchronized audio" per third party) | Official via search, plus third party |
| OpenAI | No video product | None (Sora discontinued) | n/a | n/a | Official via search |
| Runway | Active | Gen-4.5 | Not verified | Not verified | Official via search (pricing only) |
| Luma | Active | Ray3.2 (Ray3.14 also listed) | 1080p; length not verified | Not verified | Official via search (pricing only) |
| Midjourney | Active | Video model version not verified (image model V8.2) | SD and HD modes; details not verified | Not verified | Third party only |
| xAI | Active | Grok Imagine (version not verified) | 15 s, 1080p on the $100 tier per third party | Not verified | Third party and X posts |
| Pika, Adobe Firefly, Meta, Lightricks, Moonvalley | Not verified | Not verified | Not verified | Not verified | None retrieved |

### Gaps
- Not verified for any vendor: typical generation time, multi-shot generation, 9:16 vertical support, first/last-frame and reference ("ingredients") modes, and the exact audio capabilities (dialogue, effects, music).
- Google: launch date of Gemini Omni Flash; whether Omni Flash supports image-to-video, references and 9:16; whether 1080p or 4K upscaling exists in Flow and at what cost; current status of Whisk and of Veo inside Google Vids; whether Veo 3.1 is still callable in AI Studio and Vertex; whether a Veo 4 exists (no result mentioned one).
- Runway: Gen-4.5 release date, clip lengths, resolution, audio, and whether a newer model (for example a Gen-5) exists. No source mentioned one.
- Luma: Ray3.2 release date, clip lengths, audio, keyframes, HDR.
- Midjourney: current video model version, clip length, resolution, whether text-to-video and audio exist.
- xAI: current Grok Imagine version, clip length and resolution per tier, audio.
- Pika, Adobe Firefly, Meta (Vibes / Meta AI video), Lightricks LTX Studio, Moonvalley and 2026 newcomers: nothing retrieved.
- **Unverified leads from my background knowledge (roughly up to early 2026; not checked in this session; do not present as current fact):**
  - Google: Veo 3 (May 2025) introduced native audio; Veo 3.1 (October 2025) added "Ingredients to Video", first/last frame, and scene extension in Flow; native 9:16 and 1080p/4K upscaling followed around January 2026.
  - Runway: Gen-4.5 was announced on 1 December 2025; native audio and multi-shot generation were announced later that month. Aleph does video-to-video editing; Act-Two does performance capture.
  - Luma: Ray3 launched September 2025 (HDR, draft mode), Ray3 Modify (video-to-video) in December 2025.
  - Midjourney: the V1 video model (June 2025) was image-to-video only, about 5 seconds extendable to about 21 seconds, 480p with a later 720p HD mode, no audio.
  - xAI: Grok Imagine launched August 2025; version 1.0 (February 2026) made 10-second 720p clips with audio.
  - Pika: Pika 2.2 (February 2025) offered 10-second 1080p clips and keyframe transitions ("Pikaframes"); Pika 2.5 followed in 2025.
  - Adobe: the Firefly Video Model (public beta February 2025) made 5-second 1080p clips; the Firefly app also hosts partner models (Google Veo, Runway, Luma, Pika, Moonvalley and others).
  - Meta: Vibes launched 25 September 2025 as a free AI video feed in the Meta AI app, initially using partner models; Meta was reported to be building its own video model for 2026.
  - Lightricks: LTX-2 (October 2025) generates synchronized audio and video up to 4K, with open weights from January 2026. Lightricks is headquartered in Israel, not in the US or Europe. Running the open model locally needs a dedicated GPU, which the end user lacks.
  - Moonvalley: Marey (public July 2025) is trained only on licensed footage and makes 5-second 1080p clips.

## 2. Quality for stylized "3D animation" looks (independent reviews)

### Takeaway
I found no independent review or side-by-side test that judges these vendors on Pixar-like characters, product renders, isometric dioramas, clay or toy looks, or 3D motion graphics. The only evidence retrieved is general: blind-vote leaderboards are led by Chinese models, and several round-ups still rate Veo 3.1 best overall among the vendors in this scope.

### Cited Findings
- [3P] A blind-vote leaderboard put Kling v3 first for text-to-video as of November 2026 (score 1934), ahead of Happy Horse 1.0 (1816) and Seedance 2.0 Fast (1747). None of the top three is a vendor in this scope. — [LLM Stats leaderboard](https://llm-stats.com/leaderboards/best-ai-for-video-creation)
- [3P] On Artificial Analysis, Alibaba's Wan 3.0 led text-to-video with audio (1175 Elo, $0.20 per second) and ByteDance's Seedance 2.5 led image-to-video (1161 Elo), as reported on 13 November 2026. — [MarkTechPost, 13 Nov 2026](https://www.marktechpost.com/2026/11/13/best-ai-video-generation-models-2026/)
- [3P] Several 2026 round-ups name Google Veo 3.1 best overall, citing quality and native audio; one specifies the Standard tier. — [Pixflow round-up](https://pixflow.net/blog/best-ai-video-generator/); [TechJournal round-up](https://techjournal.org/best-ai-video-generators)
- [3P] Runway is commonly recommended for creative control and editing; Adobe Firefly for commercially safe output. — [SitePoint: Top 6 AI video generators in 2026](https://www.sitepoint.com/top-6-ai-video-generators-in-2026-features-strengths-and-limits/); [Pixflow round-up](https://pixflow.net/blog/best-ai-video-generator/)
- [OFF, vendor marketing] Luma advertises a real-to-cartoon video restyle. This is a vendor claim, not an independent test. — [Luma: restyle real to cartoon](https://lumalabs.ai/video-to-video/restyle-scene-from-real-to-cartoon)

### Inferences
- General leaderboards measure overall preference, mostly on realistic footage. They do not tell us which model handles stylized 3D looks best, so no ranking for the user's use case can be drawn from them.
- At least one round-up that favours Veo 3.1 refers to the Standard tier, which appears to correspond to "Veo 3.1 Quality" in Flow and leaves Flow on 5 December 2026. Those verdicts may not carry over to Veo 3.1 Lite or Omni Flash 1.2.
- The cheapest reliable way to answer this question for the user is an empirical test: run the same three or four 3D-style prompts on Google Flow's free daily credits and on any free trial credits the other vendors grant, then compare.

### Gaps
- No independent comparison of 3D-animation styles was retrieved for any vendor in scope. This key question is unanswered.
- **Unverified lead (background knowledge, not checked):** Midjourney is widely regarded as strong on stylized imagery, and its video works by animating a Midjourney image, which may suit toy, clay and diorama looks. Treat as a hypothesis to test, not a finding.

## 3. Pricing, credits and effective cost per clip

### Takeaway
On verified numbers, Google is the cheapest in scope: about $0.20 per Veo 3.1 Lite clip and $0.30 per 5-second Omni Flash clip on the $19.99 Google AI Pro plan, or roughly $2.40 to $5.76 for a finished 30-second video under the 12-generation assumption. Luma Ray3.2 matches that only at 720p ($0.30 per 5 seconds on the $30 plan); Runway Gen-4.5 costs about $0.93 to $1.44 per 5 seconds and its $15 plan cannot cover one such video.

### Cited Findings

#### Google
- [OFF] Plan prices (monthly): Google AI Plus $4.99, Google AI Pro $19.99, Google AI Ultra from $99.99, with a higher Ultra tier at $199.99. The page advertises 2x usage for Plus, 4x for Pro, and 5x or 20x for the two Ultra tiers. — [Gemini subscriptions page](https://gemini.google/subscriptions/)
- [OFF, conflicting snapshot] Another snapshot of the same page shows Plus at $7.99, Pro at $19.99 and the top Ultra tier at $249.99. The $249.99 figure predates I/O 2026; whether Plus is now $4.99 or $7.99 in the US needs a live check. — [Gemini subscriptions page (regional view)](https://gemini.google/as/subscriptions/?hl=en)
- [OFF] At I/O 2026 Google launched a new $100 AI Ultra plan and cut the top tier from $250 to $200. — [Google blog: new in Google AI subscriptions from I/O 2026](https://blog.google/products-and-platforms/products/google-one/google-ai-subscriptions/)
- [OFF] Flow credits: 50 daily credits for everyone, plus monthly credits of 200 (AI Plus), 1,000 (AI Pro), 10,000 (AI Ultra) and 25,000 (higher Ultra tier). — [Google Flow page](https://labs.google/fx/tools/flow)
- [OFF] The Google AI plans page shows the same monthly figures and lists separate Flow Music credits. — [Google AI plans](https://one.google.com/about/google-ai-plans/)
- [OFF] Omni Flash 1.2 in Flow: 1 credit per second at 360p and 3 credits per second at 720p, for videos up to 10 seconds; seconds 11 to 15 cost 6 credits each at 720p. Generating and editing are priced the same way, and these rates are for paid subscribers. — [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en); [Gemini subscriptions page](https://gemini.google/subscriptions/)
- [OFF] Veo 3.1 Lite in Flow: 10 credits per generation (5 for AI Ultra) for a 4, 6 or 8 second clip at 720p. — [Flow Help: Manage your Google Flow credits (Android view)](https://support.google.com/flow/answer/16526234?hl=en&co=GENIE.Platform%3DAndroid)
- [OFF] Older models until 5 December 2026: Veo 3.1 Fast 20 credits per generation (10 for Ultra); Veo 3.1 Quality 100 credits per 8-second video for everyone; Omni Flash 1.1 4 to 15 credits depending on length and resolution, with edits at 40 credits. — [Flow Help: Manage your Google Flow credits (Android view)](https://support.google.com/flow/answer/16526234?hl=en&co=GENIE.Platform%3DAndroid)
- [OFF] Gemini app usage is no longer a daily prompt count. It follows a "compute used" model that refreshes every five hours until a weekly cap is reached. Top-up AI credits work in Flow and Antigravity; buying them for the Gemini app was "coming soon" at I/O 2026. — [Google blog: new in Google AI subscriptions from I/O 2026](https://blog.google/products-and-platforms/products/google-one/google-ai-subscriptions/); [Google One Help: Use Google AI Ultra benefits](https://support.google.com/googleone/answer/16286513?hl=en)
- [3P] Google publishes no per-video quota for Omni Flash in the Gemini app. — [BuildFastWithAI review](https://www.buildfastwithai.com/blogs/gemini-omni-flash-review-google-ai-video-model-2026)
- [3P] Third-party guides agree on the Flow figures above (Pro $19.99 with 1,000 credits; Ultra $99.99 or $199.99; Lite 10, Fast 20, Quality 100 credits; Ultra halves Lite and Fast). One adds that lower-priority Veo 3.1 Lite costs Ultra subscribers 0 credits. — [Fello AI: Google Flow pricing](https://felloai.com/google-flow/); [CostGoat: Veo pricing, Nov 2026](https://costgoat.com/pricing/google-veo); [AIonX: Google AI Ultra limits](https://aionx.co/gemini-advanced-reviews/google-ai-ultra-limits/)
- [3P, outdated outlier] One guide still lists Ultra at $249.99 with about 1,000 credits. — [MindStudio: Flow pricing](https://www.mindstudio.ai/blog/google-flow-pricing-credits-tiers-explained)
- [OFF] Gemini API, paid tier only, per second with audio: Veo 3.1 Lite $0.05 (720p) and $0.08 (1080p); Veo 3.1 Fast $0.10 (720p), $0.12 (1080p), $0.30 (4K); Veo 3.1 Standard $0.40 (720p and 1080p), $0.60 (4K). — [Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing?hl=en)
- [3P] A developer reported being billed $0.40 for one 8-second Veo 3.1 Lite video, which confirms per-second billing. The report is about six months old. — [Google AI Developers Forum](https://discuss.ai.google.dev/t/veo-3-1-lite-pricing-shows-0-05-per-video-but-actually-costs-8-times-more/143844)

#### OpenAI
- [OFF] Nothing is on sale: the Sora app and the Sora API are discontinued. — [OpenAI Help: What to know about the Sora discontinuation](https://help.openai.com/en/articles/20001152-what-to-know-about-the-sora-discontinuation)

#### Runway
- [OFF] Prices: Standard $12 per month billed annually ($15 billed monthly); Pro $28 per month billed annually ($35 billed monthly); Max $76 per month. — [Runway pricing](https://runwayml.com/pricing)
- [3P] Max costs $95 billed monthly, so $76 is its annual-billing rate; annual billing saves 20%. — [eesel: Runway AI pricing](https://eesel.ai/blog/runway-ai-pricing); [Dupple: Runway pricing](https://dupple.com/learn/runway-pricing)
- [OFF] Monthly credits: Standard 625; Pro 2,250; Unlimited (legacy) 2,250; Max 9,500. — [Runway Help: How do credits work?](https://help.runwayml.com/hc/en-us/articles/15124877443219-How-do-credits-work); [Runway Help: Max plan details](https://help.runwayml.com/hc/en-us/articles/52067870667411-Max-plan-details)
- [OFF] Gen-4.5 costs 12 credits per second: 60 credits for 5 seconds, 120 for 10 seconds. — [Runway Help: How do credits work?](https://help.runwayml.com/hc/en-us/articles/15124877443219-How-do-credits-work)
- [OFF] Standard and Pro credits do not roll over; Max carries up to one month of unused credits. Extra credits are sold in blocks with a 1,000-credit minimum. — [Runway pricing](https://runwayml.com/pricing)
- [OFF] ProRes or PNG-sequence export adds 5 credits per second. — [Runway Help: Creating with Gen-4.5](https://help.runwayml.com/hc/en-us/articles/46974685288467-Creating-with-Gen-4-5)
- [3P] API credits are a separate wallet from app subscriptions and cost $0.01 each. — [Magic Hour: Runway Gen-4.5 pricing](https://magichour.ai/blog/runway-gen-45-pricing)
- [3P] Standard's 625 credits cover about 52 seconds of Gen-4.5; Pro's 2,250 cover about 187 seconds. — [Creatify: Runway pricing 2026](https://creatify.ai/blog/runway-pricing-%282026%29-plans-credits-and-what-you-ll-actually-pay)

#### Luma
- [OFF] Plans (monthly billing): Plus $30 with 10,000 credits; Pro $90 with 40,000 credits; Ultra $300 with 150,000 credits. Yearly billing lowers each price. — [Luma pricing](https://lumalabs.ai/pricing)
- [OFF] Ray3.2 text-to-video costs, per 5 seconds: 20 credits at 360p draft, 50 at 540p, 100 at 720p, 400 at 1080p. Video edits cost roughly 180 to 720 credits per 5 seconds depending on resolution. The dollar value of a credit depends on the plan or contract. — [Luma Agents docs: pricing](https://docs.agents.lumalabs.ai/guides/pricing/)
- [OFF, conflicting] A Luma Agents FAQ swaps the names, calling the $30 tier "Pro" and the $90 tier "Plus". The pricing page and a Luma news post use Plus $30 and Pro $90. — [Luma: FAQ about the new Luma Agents app](https://lumalabs.ai/learning-hub/frequently-asked-questions-about-the-new-luma-agents-app)
- [3P, conflicting] One tracker lists Ultra at $250 per month, not $300. — [PricingSaaS: Luma AI](https://pricingsaas.com/companies/lumaai)
- [OFF, legacy] Older Dream Machine plans are still documented: Lite $9.99 with 3,200 credits, Plus $29.99 with 10,000 credits, Unlimited $94.99. An older credit page lists Ray3 at 330 credits for 5 seconds at 1080p. These predate the current pricing. — [Luma learning hub: Dream Machine pricing information](https://lumalabs.ai/learning-hub/dream-machine-support-pricing-information); [Luma learning hub: Dream Machine credit system](https://lumalabs.ai/learning-hub/dream-machine-credit-system)
- [3P] Luma's API uses custom pricing as of September 2026. — [CostBench: Luma API](https://www.costbench.com/software/ai-media-apis/luma-dream-machine-api/)

#### Midjourney
- [3P] Basic costs $10 per month ($8 per month billed yearly) for 200 minutes of Fast GPU time. Standard costs $30 per month for 15 Fast GPU hours. — [eesel: Midjourney pricing](https://eesel.ai/blog/midjourney-pricing); [Krater: Midjourney pricing](https://krater.ai/blog/midjourney-pricing)
- [3P] Video GPU cost: about 8 minutes for an SD batch of four clips and about 26 minutes for an HD batch of four. With the batch cut to one video, about 2 minutes (SD) or 7 minutes (HD). — [Hooked: Midjourney pricing and real cost per video](https://www.hooked.so/compare/midjourney-pricing)
- [3P, conflicting] Another source says a 9-second SD video uses about 4 GPU minutes. — [FluxNote: Midjourney pricing guide](https://fluxnote.io/guides/midjourney-pricing-guide-2026)
- [3P] On the V8 image model, premium options such as HD cost about four times as much. The source does not tie this to video. — [WaveSpeed: What is Midjourney V8](https://wavespeed.ai/blog/posts/what-is-midjourney-v8-features-pricing-how-to-use-2026)

#### xAI (Grok Imagine) and the X subscription
- [SOC] On 12 October 2026 a new "X subscription" was introduced that combines Grok, X and Cursor in one plan: Plus $8, Premium $30, Super $100, Ultra $200 per month. Date decoded from the post ID. — [Sawyer Merritt on X](https://x.com/SawyerMerritt/status/2109780382870610030)
- [SOC] Bundle contents as posted. Plus: Cursor access, Grok Chat, Voice, Imagine and Build, and the Grok API. Premium adds Grok Bot, the latest Grok models, faster chat responses, "AI images and videos", and ad-free scrolling on most surfaces. Super adds about 15x Plus usage, priority access at peak times and faster generations. Ultra adds about 50x Plus usage, earliest access and the fastest generations. — [Sawyer Merritt on X](https://x.com/SawyerMerritt/status/2109780382870610030)
- [SOC] "What a tier buys is usage, not features": Plus and Ultra both run Grok Chat, Voice, Imagine and Build. Posted 13 October 2026 (date decoded from the post ID). — [Muskonomy on X](https://x.com/muskonomy/status/2109856077781283297)
- [3P] The X Subscription replaced SuperGrok and X Premium as Grok's paid plans on 12 October 2026. — [Fello AI: Grok pricing](https://felloai.com/grok-pricing/); [AI Business Weekly: What is SuperGrok](https://aibusinessweekly.net/p/what-is-supergrok)
- [3P, conflicts with the X posts] Video generation is not included on Free or on Plus ($8); it starts on Premium at $30 per month ($25 per month billed yearly). — [Aliteq: Is Grok Imagine free?](https://aliteq.com/is-grok-imagine-free); [Fello AI: Grok pricing](https://felloai.com/grok-pricing/)
- [3P] There is no published number of videos per plan. All Grok activity, including Imagine, draws on one weekly usage pool per tier, and 1080p renders use more of it than 480p. xAI's FAQ is cited as saying the single weekly pool replaced separate daily limits for Chat, Imagine, Voice and Build from June 2026. — [Aiveed: Grok video limits 2026](https://aiveed.io/blog/escape-grok-rate-limits); [Izzedo: Grok limits](https://www.izzedo.chat/blog/grok-limits)
- [3P] API price per second of video: $0.08 at 480p, $0.14 at 720p, $0.25 at 1080p. An older guide cites a flat $0.05 per second. — [BuildFastWithAI: SuperGrok video and image generation](https://blog.buildfastwithai.com/supergrok-video-image-generation-2026-speed-pricing-math-comparison); [Grok Imagine complete guide](https://aivideobootcamp.com/blog/grok-imagine-complete-guide-2026/)
- [SOC, outdated] Before the restructuring, a March 2026 post stated that X Premium+ included SuperGrok. Posted 12 March 2026 (date decoded from the post ID). — [Mark Kretschmann on X](https://x.com/mark_k/status/2032164186629759035)
- [SOC, outdated] August 2025 figures: 50 video generations per day on X Premium, 100 on Premium+ (later doubled to 200), 500 on SuperGrok Heavy; about 10 per day free. These predate the weekly pool and the new tiers. — [Grok on X, 11 Aug 2025](https://x.com/grok/status/1954994926594531713); [Muskonomy on X, 9 Aug 2025](https://x.com/muskonomy/status/1954287674363437213); [Grok on X, 22 Aug 2025](https://x.com/grok/status/1958979086510170528)
- [OFF, outdated] X's own help page still describes the old Basic, Premium and Premium+ structure. — [X Help: About X Premium](https://help.x.com/en/using-x/x-premium)

### Inferences
All figures below are my arithmetic on the cited numbers. "30-s video" = 12 generations of 8 seconds (96 generated seconds) unless noted.

**Google Flow (subscription credits)**

| Plan (monthly billing) | $ per credit | Veo 3.1 Lite clip, 4 to 8 s, 720p | Omni Flash 1.2, 5 s, 720p | Omni Flash 1.2, 8 s / 10 s, 720p | 30-s video, Veo 3.1 Lite | 30-s video, Omni Flash 720p |
|---|---|---|---|---|---|---|
| AI Plus at $4.99 (200 credits) | $0.025 | $0.25 | $0.37 | $0.60 / $0.75 | $2.99 (120 credits) | $7.19 (288 credits, more than the monthly 200) |
| AI Plus at $7.99 (200 credits) | $0.040 | $0.40 | $0.60 | $0.96 / $1.20 | $4.79 | $11.51 |
| AI Pro $19.99 (1,000 credits) | $0.020 | $0.20 | $0.30 | $0.48 / $0.60 | $2.40 (120 credits) | $5.76 (288 credits) |
| AI Ultra $99.99 (10,000 credits) | $0.010 | $0.05 | $0.15 | $0.24 / $0.30 | $0.60 (60 credits) | $2.88 |
| AI Ultra $199.99 (25,000 credits) | $0.008 | $0.04 | $0.12 | $0.19 / $0.24 | $0.48 | $2.30 |

- Other Flow rates on AI Pro: Omni Flash 1.2 at 360p costs $0.10 for 5 seconds and $1.92 for a 30-s video; a 15-second 720p Omni clip costs 60 credits ($1.20). Until 5 December 2026: Veo 3.1 Fast $0.40 per clip ($4.80 per 30-s video) and Veo 3.1 Quality $2.00 per 8-second clip ($24 per 30-s video, which is more than Pro's monthly credits).
- Capacity on AI Pro: 1,000 credits = 100 Veo 3.1 Lite generations = about 8 finished 30-s videos per month, or about 3.5 with Omni Flash at 720p. Daily free credits would add to this.
- Veo 3.1 Lite has no 5-second option in Flow; a 4, 6 or 8 second clip costs the same 10 credits.

**Google Gemini API (pay as you go)**

| Model and resolution | 8-s clip | 30-s video (96 s generated) |
|---|---|---|
| Veo 3.1 Lite 720p | $0.40 | $4.80 |
| Veo 3.1 Lite 1080p | $0.64 | $7.68 |
| Veo 3.1 Fast 720p / 1080p | $0.80 / $0.96 | $9.60 / $11.52 |
| Veo 3.1 Standard 720p or 1080p | $3.20 | $38.40 |

- Veo 3.1 Lite is about half the price through an AI Pro subscription in Flow ($0.20 per clip) compared with the API ($0.40 per 8-second clip), but only the API offers 1080p for Lite.

**Runway Gen-4.5 (12 credits per second)**

| Plan | $ per credit | 5-s clip (60 credits) | 10-s clip (120 credits) | 30-s video (1,152 credits) | Finished 30-s videos per month |
|---|---|---|---|---|---|
| Standard, monthly $15 | $0.0240 | $1.44 | $2.88 | $27.65 | 0.5 (625 credits = 52 s) |
| Standard, annual $12/mo ($144/yr) | $0.0192 | $1.15 | $2.30 | $22.12 | 0.5 |
| Pro, monthly $35 | $0.0156 | $0.93 | $1.87 | $17.92 | 1.9 |
| Pro, annual $28/mo ($336/yr) | $0.0124 | $0.75 | $1.49 | $14.34 | 1.9 |
| Max, monthly $95 | $0.0100 | $0.60 | $1.20 | $11.52 | 8.2 |
| Max, annual $76/mo ($912/yr) | $0.0080 | $0.48 | $0.96 | $9.22 | 8.2 |
| API at $0.01 per credit (third-party figure) | $0.0100 | $0.60 | $1.20 | $11.52 | n/a |

- With 10-second shots (120 generated seconds) the 30-s video needs 1,440 credits: $34.56 on Standard monthly, $22.40 on Pro monthly.
- Runway's cheaper models were not priced in the sources I retrieved, so this table overstates Runway's cost if a cheaper model is good enough.

**Luma Ray3.2 (credits per 5 seconds; I assume cost scales linearly with length)**

| Plan (monthly billing) | $ per credit | 5 s at 720p (100 credits) | 5 s at 1080p (400 credits) | 10 s at 720p / 1080p | 30-s video at 720p (1,920 credits) | 30-s video at 1080p (7,680 credits) |
|---|---|---|---|---|---|---|
| Plus $30 (10,000 credits) | $0.00300 | $0.30 | $1.20 | $0.60 / $2.40 | $5.76 | $23.04 |
| Pro $90 (40,000 credits) | $0.00225 | $0.225 | $0.90 | $0.45 / $1.80 | $4.32 | $17.28 |
| Ultra $300 (150,000 credits) | $0.00200 | $0.20 | $0.80 | $0.40 / $1.60 | $3.84 | $15.36 |

- Draft tier on Plus: 5 seconds at 360p costs $0.06 and at 540p $0.15.
- Capacity on Plus: about 5 finished 30-s videos per month at 720p, or 1.3 at 1080p.
- A cheaper Luma pattern is to iterate in draft and render only the keeper in 1080p. Four shots, each with two 8-second drafts at 360p and one 8-second final at 1080p, cost 2,816 credits, about $8.45 on Plus. I could not confirm how well a draft predicts the final render.

**Midjourney (third-party GPU-minute figures; clip length per job not confirmed)**

| Plan | $ per Fast GPU minute | One SD video (about 2 min) | One HD video (about 7 min) | HD batch of four (about 26 min) | 12 single HD generations (84 min) |
|---|---|---|---|---|---|
| Basic, monthly $10 (200 min) | $0.050 | $0.10 | $0.35 | $1.30 | $4.20 (42% of the month) |
| Basic, annual $8/mo ($96/yr) | $0.040 | $0.08 | $0.28 | $1.04 | $3.36 |
| Standard, monthly $30 (900 min) | $0.033 | $0.07 | $0.23 | $0.87 | $2.80 |

- If one job yields about 5 seconds (unverified), a 30-second video needs about 6 shots, so 18 generations: about $6.30 in HD or $1.80 in SD on Basic monthly.

**xAI Grok Imagine**

| Route | 5-s clip | 10-s clip | 30-s video (96 s generated) |
|---|---|---|---|
| API 480p ($0.08/s, third-party figure) | $0.40 | $0.80 | $7.68 |
| API 720p ($0.14/s) | $0.70 | $1.40 | $13.44 |
| API 1080p ($0.25/s) | $1.25 | $2.50 | $24.00 |
| X subscription (Plus $8, Premium $30, Super $100, Ultra $200) | Not computable: weekly usage pool, no published video count | Not computable | Not computable |

**Comparison for the end user (verified vendors only; cheapest sensible route each)**

| Vendor and route | Entry price | 5-s clip | 8 to 10-s clip | Finished 30-s video | Fit for a solo creator on a weak PC who wants low cost |
|---|---|---|---|---|---|
| Google Flow, Veo 3.1 Lite, AI Pro | $19.99/mo (or free daily credits) | $0.20 (4 or 6 s) | $0.20 (8 s) | $2.40 | Best verified cost; runs in the browser; 720p cap in Flow; 3D-style quality untested |
| Google Flow, Omni Flash 1.2 720p, AI Pro | $19.99/mo | $0.30 | $0.48 / $0.60 | $5.76 | Low cost; adds conversational editing and 15-s clips; needs a paid plan |
| Luma Ray3.2 720p, Plus | $30/mo | $0.30 | $0.60 (10 s) | $5.76 | Comparable at 720p; 1080p is four times the price |
| Midjourney HD video, Basic | $10/mo | about $0.35 per job | Not verified | about $4.20 to $6.30 | Lowest entry price; figures are third-party; length, audio and resolution unverified |
| Runway Gen-4.5, Pro | $35/mo | $0.93 | $1.87 (10 s) | $17.92 | Expensive for this profile; the $15 plan covers only 52 s of Gen-4.5 a month |
| xAI Grok Imagine, X subscription | $8 or $30/mo (conflicting) | Unknown | Unknown | Unknown | Convenient for posting on X, but allowance per plan is unpublished |
| OpenAI | n/a | n/a | n/a | n/a | Not available |

- The 12-generation assumption drives every 30-s figure. With one generation per shot the costs fall to a third; with five per shot they rise by two thirds.
- All options in scope run in the cloud, so the weak PC is not a constraint for generation. It only matters for editing and upscaling tools, which other researchers cover.

### Gaps
- Annual prices for Google AI plans, Luma, the X subscription (except Premium at $25 per month billed yearly, third party) and Midjourney's higher tiers were not retrieved.
- Whether Google AI Plus is $4.99 or $7.99 per month in the US today.
- Runway: credit rates for cheaper models, the price of top-up credits, and the Free plan's exact allowance from an official source.
- Luma: yearly prices, credits for image-to-video and for lengths other than 5 seconds, and whether a cheaper plan than $30 still exists for new users.
- Midjourney: official GPU-minute cost per video, clip length, and the prices of Pro and Mega.
- xAI: an official plan page, the real video allowance per tier, and whether the $8 Plus tier includes any video generation.
- Pika, Adobe Firefly, Meta, LTX Studio and Moonvalley: no pricing retrieved.
- **Unverified leads from my background knowledge (2025 to early 2026 prices; not checked; may be obsolete):**
  - Pika: Free (about 80 credits a month), Standard $10 per month ($8 billed yearly, 700 credits), Pro $35 ($28, 2,300 credits), Fancy $95 ($76, 6,000 credits).
  - Adobe Firefly: Standard $9.99 per month (2,000 credits), Pro $29.99 (7,000 credits), Premium $199.99 (50,000 credits); a 5-second 1080p Firefly video cost about 100 credits; partner models cost more.
  - LTX Studio: Free (one-time allowance), Lite $15 per month, Standard $35, Pro $125, metered in "computing seconds".
  - Moonvalley Marey: $14.99 (100 credits), $34.99 (250 credits) and $149.99 (1,000 credits) per month.
  - Midjourney: Standard $24, Pro $48 and Mega $96 per month on annual billing ($30, $60, $120 monthly); unlimited "relax" video on Pro and Mega.
  - Runway: Gen-4 Turbo at 5 credits per second and Aleph at 15 credits per second.
  - Meta Vibes: free to use through 2025, with paid tiers reported as planned for 2026.

## 4. Free tiers

### Takeaway
The only confirmed recurring free allowance is Google Flow's 50 credits per day, which would cover five Veo 3.1 Lite generations a day if free accounts can select that model (not confirmed). Runway gives 125 one-time credits without Gen-4.5; Luma, Midjourney and xAI appear to have no usable free video tier; OpenAI has none.

### Cited Findings
- [OFF] Google Flow gives 50 daily credits to everyone, with or without a subscription. — [Google Flow page](https://labs.google/fx/tools/flow); [Fello AI: Google Flow pricing](https://felloai.com/google-flow/)
- [OFF] Veo 3.1 Lite costs 10 credits per generation for everyone who is not an Ultra subscriber. — [Flow Help: Manage your Google Flow credits (Android view)](https://support.google.com/flow/answer/16526234?hl=en&co=GENIE.Platform%3DAndroid)
- [OFF and 3P] Omni Flash needs a paid plan: Google's page says its per-second rates are for paid subscribers, and third-party guides say Omni Flash requires AI Plus, Pro or Ultra in both the Gemini app and Flow. — [Gemini subscriptions page](https://gemini.google/subscriptions/); [GeoToolbox guide](https://geotoolbox.ai/blog/gemini-omni)
- [OFF] The Gemini API has no free tier for any Veo 3.1 variant. — [Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing?hl=en)
- [3P] Runway's Free plan gives 125 one-time credits and does not include every paid model; Gen-4.5 needs Standard or higher. — [Magic Hour: Runway Gen-4.5 pricing](https://magichour.ai/blog/runway-gen-45-pricing); [Magic Hour: Runway free plan](https://magichour.ai/blog/runway-ml-pricing)
- [3P] Luma's current pricing page shows no permanent free plan; new accounts may get limited trial credits. — [Magic Hour: Luma AI pricing](https://magichour.ai/blog/luma-dream-machine-pricing)
- [OFF] Luma's own machine-readable summary says "Free trial credits included on all plans", without a number. — [Luma: official information for AI assistants](https://lumalabs.ai/llm-info)
- [3P] Midjourney has no free plan. — [eesel: Midjourney pricing](https://eesel.ai/blog/midjourney-pricing)
- [3P] Grok: video generation is not included on the Free tier (and, per the same sources, not on the $8 Plus tier). — [Aliteq: Is Grok Imagine free?](https://aliteq.com/is-grok-imagine-free)
- [OFF] OpenAI: no free or paid video generation since the Sora shutdown. — [OpenAI Help: What to know about the Sora discontinuation](https://help.openai.com/en/articles/20001152-what-to-know-about-the-sora-discontinuation)

### Inferences
- If free Flow accounts can use Veo 3.1 Lite, 50 daily credits equal five 720p clips with audio per day, and the 12 generations for one 30-second video take about three days at no cost. This is the strongest free option found, but the model access for free accounts is not confirmed.
- 125 one-time Runway credits equal about 10 seconds of a 12-credit-per-second model, so the Runway free plan is a trial, not a production tier.

### Gaps
- For every vendor: watermark on free output, resolution cap, queue speed and whether a payment card is required. None of this was retrieved.
- Google: which models free Flow accounts may use, whether free output carries a visible watermark, and whether the Gemini app offers any free video generation.
- Pika, Adobe Firefly, Meta, LTX Studio and Moonvalley free tiers: not retrieved.
- **Unverified leads (background knowledge, not checked):** in 2025 Pika had a free plan with a small monthly credit grant and a watermark; Meta's Vibes and Meta AI video were free; Adobe Firefly's free tier allowed only a handful of video generations; LTX Studio's free tier was a one-time allowance for personal use.

## 5. Usage rights, watermarks and provenance

### Takeaway
Almost nothing on usage rights could be verified. The single confirmed point is that Google's Omni Flash output carries a SynthID invisible watermark (third-party report).

### Cited Findings
- [3P] Gemini Omni Flash video is SynthID-watermarked. — [WaveSpeed: "Gemini Omni Flash Shipped"](https://wavespeed.ai/blog/posts/gemini-omni-flash-shipped-what-actually-launched/)
- [3P] Round-ups position Adobe Firefly as the commercially safe choice. — [Pixflow round-up](https://pixflow.net/blog/best-ai-video-generator/)
- [3P] Midjourney is discussed as carrying copyright risk in a September 2026 review of whether it is still worth paying for. — [Tapbit, 9 Sep 2026](https://www.tapbit.com/en/learn/article/midjourney-pricing-features-2026-20260909)

### Inferences
- Because rights terms differ by plan at several vendors, the user should not assume that the cheapest plan allows commercial use or removes the watermark. This must be checked on each vendor's terms before choosing a plan.

### Gaps
- Commercial-use rights per plan, visible watermark removal, and invisible watermark or C2PA metadata were not retrieved for any vendor.
- **Unverified leads (background knowledge to early 2026, not checked):**
  - Google: all Veo output carried SynthID; a visible watermark appeared on video from plans below Ultra.
  - Runway: paid plans removed the watermark; the free plan was watermarked.
  - Luma: free and the old Lite plan were non-commercial; commercial use started at the old Plus plan.
  - Pika: commercial use and watermark-free downloads started at the Pro plan.
  - Midjourney: paid subscribers could use output commercially (larger companies needed Pro or Mega); no visible watermark; output public by default.
  - Adobe Firefly: Content Credentials (C2PA) attached to output; the "commercially safe" promise covered Adobe's own model, not partner models.
  - LTX Studio: commercial licence started at the Standard plan.
  - Moonvalley: Marey marketed as trained only on licensed data.

## 6. Restrictions (regions, age, content)

### Takeaway
No regional, age or content restriction could be verified in this session. The only access rule confirmed is that Omni Flash video in the Gemini app and Flow requires a paid Google AI plan.

### Cited Findings
- [3P] Omni Flash in the Gemini app and Flow requires a Google AI Plus, Pro or Ultra subscription. — [GeoToolbox guide](https://geotoolbox.ai/blog/gemini-omni)
- [3P, speculation] Commentary links Sora's shutdown to deepfake concerns and weak economics; OpenAI itself gave no specific reason. — [TechJournal: What happened to Sora](https://techjournal.org/what-happened-to-sora-openai-shutdown)
- [OFF] Google publishes country-specific versions of its AI plans page, for example for the UK and New Zealand. — [Google AI plans, UK](https://one.google.com/intl/en_uk/about/google-ai-plans/); [Google AI plans, New Zealand](https://one.google.com/intl/en_nz/about/google-ai-plans/)

### Inferences
- Google's plan prices and availability probably differ by country, since the plans page is localized. The US dollar prices in this file may not be what a buyer outside the US sees.
- If the user is in the EU/EEA or the UK, availability must be confirmed for each product before subscribing. Several of these services launched features later in Europe in the past.

### Gaps
- EU/EEA and UK availability, age or ID verification, and rules on real people, logos and copyrighted characters were not retrieved for any vendor.
- **Unverified leads (background knowledge to early 2026, not checked):**
  - Google: video generation in the Gemini app was limited to adults; photo-to-video launched later in the EEA, Switzerland and the UK.
  - xAI: after the January 2026 scandal over sexualized images of real people, image generation and editing on X were limited to paying subscribers, and regulators in the EU and UK opened investigations.
  - Meta: Vibes reached Europe in late 2025, after the US launch.

## 7. What changed during 2026

### Takeaway
2026 removed OpenAI from the market and restructured the others: Google added Omni Flash, re-tiered Ultra and is retiring Veo 3.1 Fast and Quality from Flow; xAI folded SuperGrok and X Premium into one X subscription; Runway replaced Unlimited with Max; Luma moved to Ray3.2 with $30, $90 and $300 plans.

### Cited Findings
- [3P] 24 March 2026: OpenAI announced it was discontinuing Sora (app and API). — [Wikipedia: Sora](https://en.wikipedia.org/wiki/Sora_%28text-to-video_model%29)
- [OFF] 26 April 2026: Sora web and app discontinued. 24 September 2026: Sora API discontinued. — [OpenAI Help: What to know about the Sora discontinuation](https://help.openai.com/en/articles/20001152-what-to-know-about-the-sora-discontinuation)
- [OFF] Google I/O 2026: new $100 AI Ultra plan; top Ultra tier cut from $250 to $200; Gemini app limits moved to a compute-based model with a five-hour refresh and weekly cap. — [Google blog: new in Google AI subscriptions from I/O 2026](https://blog.google/products-and-platforms/products/google-one/google-ai-subscriptions/)
- [3P] Gemini Omni Flash replaced Veo 3.1 as the Gemini app's default video model (launch date not retrieved; the coverage is dated 2026); version 1.2 followed on 5 November 2026. — [Apidog: Gemini Omni 1.2 Flash or Veo](https://apidog.com/blog/gemini-omni-1-2-flash-or-veo/); [BuildFastWithAI review](https://www.buildfastwithai.com/blogs/gemini-omni-flash-review-google-ai-video-model-2026)
- [3P] 22 October 2026: Veo Preview models reported shut down in the Gemini API. — [Apidog: Gemini Omni 1.2 Flash or Veo](https://apidog.com/blog/gemini-omni-1-2-flash-or-veo/)
- [OFF] 5 December 2026 (upcoming): Veo 3.1 Fast, Veo 3.1 Quality and Omni Flash 1.1 retire from Flow. — [Flow Help: models and supported features](https://support.google.com/flow/answer/16352836?hl=en)
- [3P] June 2026: Grok replaced separate daily limits with one weekly usage pool. — [Izzedo: Grok limits](https://www.izzedo.chat/blog/grok-limits)
- [SOC] 12 October 2026: the X subscription (Plus $8, Premium $30, Super $100, Ultra $200) replaced SuperGrok and X Premium and bundled Cursor. — [Sawyer Merritt on X](https://x.com/SawyerMerritt/status/2109780382870610030)
- [3P] 1 June 2026: Runway stopped selling the Unlimited plan and introduced Max. — [Dupple: Runway pricing](https://dupple.com/learn/runway-pricing); [eesel: Runway AI pricing](https://eesel.ai/blog/runway-ai-pricing)
- [3P] January 2026: Luma released Ray 3.14. — [Magic Hour: Luma AI pricing](https://magichour.ai/blog/luma-dream-machine-pricing)
- [OFF] Luma now sells Plus $30, Pro $90 and Ultra $300 with Ray3.2, replacing the Dream Machine-era Lite $9.99, Plus $29.99 and Unlimited $94.99 plans. — [Luma pricing](https://lumalabs.ai/pricing); [Luma learning hub: Dream Machine pricing information](https://lumalabs.ai/learning-hub/dream-machine-support-pricing-information)
- [3P] 17 March 2026: Midjourney V8 alpha; V8.2 default by September 2026. — [WaveSpeed: What is Midjourney V8](https://wavespeed.ai/blog/posts/what-is-midjourney-v8-features-pricing-how-to-use-2026); [Tapbit, 9 Sep 2026](https://www.tapbit.com/en/learn/article/midjourney-pricing-features-2026-20260909)
- [3P] By November 2026 Chinese models (Kling v3, Wan 3.0, Seedance 2.5) lead the public video leaderboards. — [LLM Stats leaderboard](https://llm-stats.com/leaderboards/best-ai-for-video-creation); [MarkTechPost, 13 Nov 2026](https://www.marktechpost.com/2026/11/13/best-ai-video-generation-models-2026/)

### Inferences
- Luma's cheapest plan appears to have risen from $9.99 to $30 (timing not confirmed, probably 2026), which removes it as a low-budget option unless legacy plans remain available.
- Runway's removal of the Unlimited plan ends the flat-rate route that heavy users relied on; every Gen-4.5 second is now metered unless Max's allowance is enough.
- The pace of change (three Omni Flash versions and a retirement date inside one year at Google) means any plan choice should be on monthly billing, not annual, until the line-up settles.

### Gaps
- The launch dates of Gemini Omni Flash, Veo 3.1 Lite and Ray3.2 were not retrieved.
- 2026 changes at Pika, Adobe Firefly, Meta, Lightricks and Moonvalley were not retrieved.
- Important 2026 newcomers from the US or Europe: none identified. The only unfamiliar name in the leaderboards, Happy Horse 1.0, was not attributed to a company in the results (background knowledge suggests a Chinese origin, unverified).
- **Unverified leads (background knowledge, not checked):** Black Forest Labs (Germany) was reported to be working on a video model; Meta was reported to be testing a standalone Vibes app and paid tiers in early 2026; Adobe and Runway announced a partnership in December 2025 that brought Runway models into Firefly.
