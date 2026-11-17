# Google Flow, the Gemini app and Nano Banana: verified cost and limits as of 17 November 2026

> **Read this first: how these notes were made.**
> 1. This is the second, verification round for the Google route. I opened Google's own pages directly (about 80 page loads on `support.google.com`, `gemini.google` and `labs.google`) on **17 November 2026** and read the full text and tables, not search snippets.
> 2. **Evidence tags.** `READ DIRECTLY 17 Nov 2026` = I read the linked page itself on that date. `SEARCH SUMMARY` = a web-search summary only; the page was not opened (11 searches used, only for things the readable hosts did not answer). Each search returns one summary covering about ten pages, so for SEARCH SUMMARY items I link the most likely source page or pages.
> 3. **Verdict words** compare with the first-round file `first_party_video_models_western.md`: **Confirms**, **Corrects**, **Contradicts**, or **New** (not in the first round).
> 4. **Hosts I could not read** (blocked by network policy): `flow.google.com` (the Flow product and its pricing page; `labs.google/fx/tools/flow` now redirects there), `one.google.com`, `policies.google.com`, `blog.google`, and `ai.google.dev` (redirects to `aistudio.google.com`). Figures that live only on those pages are SEARCH SUMMARY or listed under Gaps.
> 5. Google's help pages show no "last updated" date in their page source, so I can give the date read but not the date written. Google states on the pages that credit costs and limits can change at any time.
> 6. Saved copies of every page (raw HTML and extracted text) are in the session scratch folder `/tmp/claude-0/-home-user-Ivaylo/58e18699-43b7-519e-878f-a17fb3cfeb75/scratchpad/google_route/` (temporary; it may be cleared).
>
> **Scoreboard against the first round (details and links in the sections below).**
>
> | First-round figure or claim | Verdict | What Google's page says on 17 Nov 2026 |
> |---|---|---|
> | Google AI Plus is $4.99 or $7.99 a month | **Resolved: $4.99** | US page shows $4.99. The $7.99 figure is on the American Samoa regional page, which is out of date. Search coverage dates the US cut from $7.99 to $4.99 to 8 June 2026. |
> | Ultra is $99.99 or $199.99 (or $249.99) | **Resolved: both** | Two Ultra tiers: $99.99 ("5x") and $199.99 ("20x"). $249.99 appears only on the out-of-date American Samoa page. |
> | AI Pro $19.99 | **Confirms** | $19.99 a month. |
> | 50 daily Flow credits for everyone; 200 / 1,000 / 10,000 / 25,000 monthly | **Confirms** | Same numbers. Daily and monthly credits do not roll over. |
> | Veo 3.1 Lite: 10 credits (5 for Ultra), 4, 6 or 8 s, 720p | **Confirms** | Same. Available to all users, including free. |
> | Omni Flash 1.2: 1 credit/s at 360p, 3 credits/s at 720p; seconds 11 to 15 cost 6 credits each at 720p | **Confirms** | Same. Adds: at 360p, seconds 11 to 15 cost 2 credits each. |
> | Omni Flash rates are "for paid subscribers"; Omni Flash needs a paid plan | **Contradicts (for Flow)** | In Flow, "All users" can generate or edit Omni Flash 1.2 video up to 10 s. Only seconds 11 to 15, Extend and upscaling need a plan. In the Gemini app, video does need a plan. |
> | Veo 3.1 Fast 20 credits, Quality 100, Omni Flash 1.1 4 to 15, edits 40 | **Confirms** | Same table, valid until 5 December 2026. |
> | Veo 3.1 Fast, Quality and Omni Flash 1.1 leave Flow on 5 December 2026 | **Confirms** | Stated on two Flow help pages. Veo Extend was already retired on 5 November 2026. |
> | Third-party: lower-priority Veo 3.1 Lite costs Ultra subscribers 0 credits | **Corrects** | 0 credits only for "Ultra 20x subscribers & family plan managers". |
> | Resolution conflict: 720p only, or upscaling to 1080p / 4K | **Resolved** | Generation is 360p or 720p. Subscribers upscale to 720p or 1080p for 0 credits (clips up to 10 s). 4K is Ultra only, 50 credits. |
> | Third-party: scene extension reaches 40 s in 10-s steps | **Not confirmed** | Flow: extend by 3 to 10 s per step (subscribers, Omni Flash 1.2). No maximum total length is stated. |
> | Gemini app limits are compute-based, refresh every five hours, weekly cap; no per-video quota | **Confirms** | Same. Plus = 2x, Pro = 4x the standard limits; Ultra = 5x or 20x Pro. |
> | Gap: can free Flow accounts use Veo 3.1 Lite? | **Answered: yes** | Also Omni Flash 1.2 up to 10 s. |
> | Gap: visible watermark on free output? | **Answered** | Visible watermark is a user setting. It is forced only in India, South Korea and Vietnam (unless on the top Ultra plan). SynthID is always embedded. |
> | Gap: does the Gemini app offer free video generation? | **Answered: no** | Video generation needs a Google AI plan and age 18+. |
> | Gap: EU/EEA and UK availability | **Answered** | Flow lists all 27 EU states, Iceland, Liechtenstein, Norway, Switzerland and the UK. Two features are off there: editing uploaded videos, and avatars. |
> | Unverified lead: visible watermark on plans below Ultra | **Out of date** | See the watermark row above. |
> | Gap: status of Whisk | **Answered (partly)** | `labs.google/fx/tools/whisk` now redirects to `flow.google.com/?from=whisk`. |

## 1. Flow credit cost per generation (video models, edits, extensions, upscaling, images)

### Takeaway
Flow now has two current video models with different billing: Omni Flash 1.2 is charged per second (1 credit at 360p, 3 credits at 720p) and Veo 3.1 Lite is charged per clip (10 credits for a 4, 6 or 8 second 720p clip). Images cost no credits at all, and subscribers can upscale clips of up to 10 seconds to 1080p for 0 credits.

### Cited Findings

**Omni Flash 1.2 (current model)**
- Generate or edit videos up to 10 s, "All users": 360p = 1 credit per second; 720p = 3 credits per second. **Confirms** the first-round rates; **contradicts** the first-round note that these rates are for paid subscribers only. — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- Generate or edit videos up to 15 s, "Google AI Plus, Pro, & Ultra subscribers only": 360p = 1 credit per second up to 10 s, then 2 credits per extra second for seconds 11 to 15; 720p = 3 credits per second up to 10 s, then 6 credits per extra second for seconds 11 to 15. **Confirms** the 720p figure; the 360p surcharge is **new**. — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- Extend videos by 3 to 10 s, subscribers only: 1 credit per second added at 360p, 3 credits per second added at 720p. **New.** — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- Upscale videos to 720p or 1080p, subscribers only: 0 credits for clips of 1 to 10 s, then 1 credit per extra second over 10 s. **New; answers the first-round gap on upscaling cost.** — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- Upscale videos to 4K, "Google AI Ultra subscribers only": 50 credits flat for 1 to 10 s, then 5 credits per extra second over 10 s. **New.** — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- Edits are priced like generations: "Edits cost the same credits per second as standard generations." — READ DIRECTLY 17 Nov 2026: [Flow Help: Edit videos & build scenes](https://support.google.com/flow/answer/16935718?hl=en)
- Google describes Omni 360p as generating or editing "at one-third the credit cost of 720p". — READ DIRECTLY 17 Nov 2026: [Flow Help: models & supported features](https://support.google.com/flow/answer/16352836?hl=en)

**Veo 3.1 Lite (current model)**
- "With Veo 3.1 Lite, all users can generate 4s, 6s, or 8s videos in 720p." Cost per generation: 5 credits for Google AI Ultra subscribers, 10 credits for all other users. The price is the same for 4, 6 or 8 seconds. **Confirms.** — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- "Lower Priority mode" for Veo 3.1 Lite costs 0 credits, but only for "Ultra 20x subscribers & family plan managers". **Corrects** the first-round third-party claim that it is free for all Ultra subscribers. — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)

**Retiring models (available at these rates until 5 December 2026)**
- Veo 3.1 Fast (4, 6, 8 s): 20 credits, or 10 for Ultra. Veo 3.1 Quality (8 s): 100 credits for all users. **Confirms.** — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- Omni Flash 1.1 at 720p: 4 s = 7, 6 s = 10, 8 s = 12, 10 s = 15 credits. At 360p: 4 s = 4, 6 s = 5, 8 s = 6, 10 s = 7 credits. Editing an uploaded or generated video with Omni Flash 1.1: 40 credits for any length or resolution. **Confirms** the first-round range of 4 to 15 and the 40-credit edit. — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- "All retiring models": 1080p upscaling costs 0 credits for Plus, Pro and Ultra subscribers and is "Not available" to non-subscribers; 4K upscaling costs 50 credits and is Ultra only. — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)

**Rules that affect what you pay**
- Costs are "per generation, not per request"; one request "may generate 2 videos", and each is charged. The number of outputs is a setting in the prompt box. — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en); [Flow Help: Create videos](https://support.google.com/flow/answer/16353334?hl=en)
- Credits are deducted when a generation starts. If it fails or hits a safety filter, the credits "are returned to you within one hour". — READ DIRECTLY 17 Nov 2026: [Flow Help: Get started](https://support.google.com/flow/answer/16353333?hl=en)
- If audio generation fails, the video is not produced and credits are refunded, unless the project setting "Return silent videos" is on, in which case the silent video is returned and charged as usual. — READ DIRECTLY 17 Nov 2026: [Flow Help: Get started](https://support.google.com/flow/answer/16353333?hl=en)
- "Limits are subject to change at any time. To find the latest costs, at the top right of your prompt box, click Settings." — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- Flow Agent chat queries cost no credits but have a daily limit per plan; media the Agent generates does use credits, and by default the Agent asks before spending them. — READ DIRECTLY 17 Nov 2026: [Flow Help: Use the Google Flow Agent](https://support.google.com/flow/answer/17093911?hl=en)

**Image generation inside Flow (Nano Banana)**
- "Generating and upscaling images in Google Flow does not currently use your monthly Google Flow credits or AI credits. Instead, each Google AI plan has a daily image generation limit per model." **New.** — READ DIRECTLY 17 Nov 2026: [Flow Help: Create & edit images](https://support.google.com/flow/answer/16729550?hl=en)
- Daily image limits in Flow, read from the page's table (**new**) — READ DIRECTLY 17 Nov 2026: [Flow Help: Create & edit images](https://support.google.com/flow/answer/16729550?hl=en):

| Model | Without a Google AI plan | Google AI Plus & Pro | Google AI Ultra |
|---|---|---|---|
| Nano Banana Pro | Up to 20 / day | Up to 100 / day | Up to 500 / day |
| Nano Banana 2.1 + Nano Banana 2 Lite (one shared pool) | Up to 400 / day | Up to 1,000 / day | Up to 1,000 / day |
| 2K upscale | Up to 200 / day | Up to 200 / day | Up to 200 / day |
| 4K upscale | Not available | Not available | Up to 200 / day |

- The image limit resets 24 hours after the first generation with that model or shared pool. Failed or blocked generations do not count. — READ DIRECTLY 17 Nov 2026: [Flow Help: Create & edit images](https://support.google.com/flow/answer/16729550?hl=en)
- Flow's three image models: Nano Banana Pro ("default model for Google AI Ultra subscribers"), Nano Banana 2 Lite ("the default model available at no charge") and Nano Banana 2.1 ("the standard model"). — READ DIRECTLY 17 Nov 2026: [Flow Help: models & supported features](https://support.google.com/flow/answer/16352836?hl=en)

### Inferences
- Credits for common Omni Flash 1.2 clip lengths (my arithmetic from the page's per-second rates): 4 s = 4 credits at 360p or 12 at 720p; 5 s = 5 or 15; 8 s = 8 or 24; 10 s = 10 or 30; 15 s = 20 or 60 (subscribers only).
- For an 8-second 720p clip, Veo 3.1 Lite (10 credits) costs less than half of Omni Flash 1.2 at 720p (24 credits). The cheapest route of all is Omni Flash 1.2 at 360p (8 credits), which a subscriber can then upscale to 720p or 1080p for 0 credits. Whether an upscaled 360p clip looks as good as a native 720p clip is not something Google's pages state.
- A 4-second Veo 3.1 Lite clip costs the same 10 credits as an 8-second one, so there is no saving in generating short Lite clips.
- Set "number of outputs" to 1. With 2 outputs, every request costs double.
- Still keyframes are effectively free in Flow: up to 400 images a day on the standard models and 20 a day on Nano Banana Pro without any plan.

### Gaps
- **Can Veo 3.1 Lite clips be upscaled to 1080p?** The page is ambiguous. The Veo 3.1 Lite table lists only 720p generation, and the upscaling rows sit in the Omni Flash 1.2 table and in a row labelled "All retiring models" (Lite is not retiring, yet it is listed in that same table). The models page lists upscaling only as "Upscale Omni 360p videos". Treat Lite as 720p only until checked in the product.
- I could not open the in-product settings panel, which Google names as the place for the "latest costs" (`flow.google.com` is blocked).
- Not published on the pages read: the daily number of Agent queries, the base pixel size of Flow images, and video frame rate or bitrate.

## 2. Credits per plan, rollover, top-ups and plan prices

### Takeaway
On Google's US page on 17 November 2026 the monthly prices are $0 (free), $4.99 (AI Plus), $19.99 (AI Pro) and $99.99 or $199.99 (the two AI Ultra tiers). Everyone gets 50 Flow credits a day; subscribers also get 200, 1,000, 10,000 or 25,000 a month; nothing rolls over; and extra "AI credits" can be bought only on Pro and Ultra.

### Cited Findings

**Plan prices (United States, monthly)**
- Free: "$0/ month with a Google Account". Google AI Plus: "$4.99/ month" ("Get 2x higher usage access than Free", 400 GB storage). Google AI Pro: "$19.99/ month" ("4x higher usage access than Free", 5 TB storage). Google AI Ultra: "Starting at $99.99/ month"; "$99.99/ month: 5x higher usage limits vs. AI Pro; $199.99 / month: 20x higher usage limits vs. AI Pro". The page's region picker reads "United States". **Confirms** the first-round main snapshot. Note that 5x and 20x are measured against AI Pro, not against Free. — READ DIRECTLY 17 Nov 2026: [Gemini subscriptions page (US)](https://gemini.google/subscriptions/); identical content at [gemini.google/us/subscriptions](https://gemini.google/us/subscriptions/?hl=en)
- The conflicting first-round snapshot comes from the American Samoa regional page. It shows Plus "$ 7.99 USD", Pro "$ 19.99 USD", the lower Ultra tier as "$ NaN USD" (a display error) and the top Ultra tier "$ 249.99 USD". These are pre-June 2026 prices on a page that has not been updated. **Resolves the first-round conflict: the US price of AI Plus is $4.99, and Ultra has two tiers at $99.99 and $199.99.** — READ DIRECTLY 17 Nov 2026: [Gemini subscriptions page (American Samoa)](https://gemini.google/as/subscriptions/?hl=en)
- Google cut AI Plus in the US from $7.99 to $4.99 a month and doubled its storage from 200 GB to 400 GB, announced 8 June 2026. — SEARCH SUMMARY: [TechCrunch, 9 June 2026](https://techcrunch.com/2026/06/09/google-just-fired-a-warning-shot-in-the-ai-subscription-price-wars); [Engadget](https://engadget.com/2190039/google-cuts-the-price-of-its-ai-plus-plan-and-doubles-the-storage)
- Regional prices for context (monthly; the Flow credit amounts on these pages are the same as in the US) — READ DIRECTLY 17 Nov 2026: [Bulgaria](https://gemini.google/bg/subscriptions/?hl=bg); [Germany](https://gemini.google/de/subscriptions/?hl=de); [Ireland](https://gemini.google/ie/subscriptions/?hl=en-GB); [United Kingdom](https://gemini.google/gb/subscriptions/?hl=en-GB):

| Country page | AI Plus | AI Pro | AI Ultra 5x | AI Ultra 20x |
|---|---|---|---|---|
| United States | $4.99 | $19.99 | $99.99 | $199.99 |
| Bulgaria | 4,99 € | 21,98 € | 106,86 € | 219,85 € |
| Germany, Ireland | €4.99 | €21.99 | €99.99 | €219.99 |
| United Kingdom | £4.49 | £18.99 | £79.99 | £189.99 |

- The July 2026 Google One price increase applied only to Algeria, Egypt, Nigeria, Pakistan and Turkey. — READ DIRECTLY 17 Nov 2026: [Google One Help: price update July 2026](https://support.google.com/googleone/answer/17251824?hl=en)
- Plans come in storage variants: AI Plus with 400 GB or 2 TB; AI Pro with 5 TB or 10 TB; AI Ultra 5x with 20 TB and Ultra 20x with 30 TB. AI Pro can be bought monthly or annually. Prices of the larger variants and of annual billing are not on the pages read. — READ DIRECTLY 17 Nov 2026: [Google One Help: Get AI Plus](https://support.google.com/googleone/answer/16548195?hl=en); [Get AI Pro](https://support.google.com/googleone/answer/16476811?hl=en); [Get AI Ultra](https://support.google.com/googleone/answer/16476748?hl=en)

**Flow credits per plan**
- "With or without a subscription, you receive 50 Google Flow credits per day." Subscribers receive extra monthly credits: AI Plus 200, AI Pro 1,000, "AI Ultra $100" 10,000, "AI Ultra $200" 25,000. **Confirms.** Subscribers keep the 50 daily credits on top of the monthly pool. — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- The plan cards repeat the same amounts: "Get 200 Google Flow Credits" (Plus), "1,000" (Pro), "10,000 or 25,000" (Ultra), each "with access to Gemini Omni Flash and custom tool creation". The free card says Flow access includes "limited access to Nano Banana Pro". — READ DIRECTLY 17 Nov 2026: [Gemini subscriptions page (US)](https://gemini.google/subscriptions/)
- Daily credits: the refresh "is triggered by your first generation" (first use on 12 August means the next 50 arrive on 13 August), and "the unused Google Flow credits don't roll over". **New detail.** — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- Monthly credits "refresh at the start of your billing cycle" and "Unused monthly Google Flow credits do not roll over to the next month." **New detail.** — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- Qualifying Google Workspace accounts get Flow "at no extra charge" with 50 daily credits. — READ DIRECTLY 17 Nov 2026: [Flow Help: Get started](https://support.google.com/flow/answer/16353333?hl=en)
- Credits are shared across devices on one account, and AI credits can be shared with a Google One family group. — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)

**Top-ups ("AI credits")**
- "AI credits are only available for Google AI Pro and Google AI Ultra plans." "AI credits are not available for purchase for Google AI Plus plans." Not sold in Japan. Offered amounts: "e.g., 2,500, 5,000, or 20,000 AI credits", as a one-time purchase or with auto-reload (at most 5 auto-reloads a day). They work in Google Flow and Google Antigravity. **Confirms** that top-ups exist; the Plus exclusion is **new**. — READ DIRECTLY 17 Nov 2026: [Google One Help: Purchase Google AI credits](https://support.google.com/googleone/answer/17103110?hl=en); [Google One Help: Use Google AI Plus benefits](https://support.google.com/googleone/answer/16882689?hl=en)
- Conflict inside Google's own pages: the Flow credits page says "Plus, Pro, and Ultra subscribers can purchase AI credits", while the two Google One pages above say Plus cannot. Google One is the seller, so its wording is the safer reading. — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- "AI credits may expire after a certain period, as set out when you acquire them." Members who subscribed through a third party, Pixel Pass or Apple billing cannot buy them. — READ DIRECTLY 17 Nov 2026: [Google One Help: Manage your AI credits](https://support.google.com/googleone/answer/16287445?hl=en)
- Top-up price: $25 for 2,500 credits, $50 for 5,000 and $200 for 20,000 (1 cent per credit), with the balance valid for 12 months from the last purchase. The live help page I read lists the amounts but **no prices and no 12-month term**, so these dollar figures rest on a search summary that appears to draw on an older version of the page. — SEARCH SUMMARY: [Google One Help: Purchase Google AI credits (search-indexed version)](https://support.google.com/googleone/answer/17103110?hl=en-MY); [Google blog: Flow and Whisk AI credits update](https://blog.google/technology/google-labs/flow-whisk-ai-credits-update/)

### Inferences
- Value of one monthly credit (plan price divided by monthly credits; my arithmetic): AI Plus $0.02495, AI Pro $0.01999, Ultra 5x $0.0100, Ultra 20x $0.0080. A top-up credit would cost $0.0100 if the search-summary price is still right.
- The 50 daily credits add up to as much as 1,500 credits in a 30-day month if used every day. That is more than the 1,000 monthly credits of AI Pro. For a patient creator the free daily allowance is the largest pool below Ultra.
- Because nothing rolls over, a plan only pays off in months when the credits are actually spent. Monthly billing fits better than annual billing for an irregular workload.

### Gaps
- US dollar price of top-up credits on a live Google page (the price is shown only inside Google One, which I could not open).
- Which pool is spent first, the daily 50 or the monthly credits. Google's pages do not say, and a search found no source.
- Annual prices, and prices for AI Plus 2 TB and AI Pro 10 TB.
- Whether any free trial of AI Plus or AI Pro is on offer today. The trials page gives rules but no current offers. — READ DIRECTLY 17 Nov 2026: [Google One Help: Learn about Google One trials](https://support.google.com/googleone/answer/9155746?hl=en)

## 3. What a free (non-subscriber) user can generate

### Takeaway
A free adult user in a supported country gets 50 Flow credits a day and can use both current video models: Veo 3.1 Lite (4, 6 or 8 s at 720p, 10 credits) and Omni Flash 1.2 (3 to 10 s at 360p or 720p, charged per second), plus image generation that costs no credits. Free users cannot extend, upscale or make 15-second clips, and may be blocked from video generation at peak hours.

### Cited Findings
- "With no subscription: Access basic video generation and editing features and 50 Google Flow credits per day to try Google Flow." — READ DIRECTLY 17 Nov 2026: [Flow Help: Get started](https://support.google.com/flow/answer/16353333?hl=en)
- Omni Flash 1.2 "Without a Google AI subscription": Text to Video, Frames to Video (web only), Ingredients/References to Video and Video to Video editing, each in "both aspect ratios" and "3 to 10s video length". "All users can access Omni Flash models." **Contradicts** the first-round finding that Omni Flash needs a paid plan (true only for the Gemini app). — READ DIRECTLY 17 Nov 2026: [Flow Help: models & supported features](https://support.google.com/flow/answer/16352836?hl=en)
- Veo 3.1 Lite: "all users can generate 4s, 6s, or 8s videos in 720p"; non-Ultra users pay 10 credits. **Answers the first-round gap** on whether free accounts can select Lite. — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- Subscriber-only features, so not available free: clips of 11 to 15 s, Extend, upscaling to 720p or 1080p, and building custom Tools (free users can still use pre-built Tools). — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en); [Flow Help: Create & manage Tools](https://support.google.com/flow/answer/17104535?hl=en)
- Peak-hour limit: "During peak hours, roughly 2 PM to 5 PM UTC, you may not be able to generate videos without a subscription. You can still generate images and use the Google Flow Agent." **New.** — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- Rate limiting: after "a large number of generations in a day, the number of generations you can make within a minute will decrease". — READ DIRECTLY 17 Nov 2026: [Flow Help: Get started](https://support.google.com/flow/answer/16353333?hl=en)
- Free image allowance in Flow: up to 20 Nano Banana Pro images a day, up to 400 a day on Nano Banana 2.1 and 2 Lite combined, and up to 200 2K upscales a day, with no credits charged. — READ DIRECTLY 17 Nov 2026: [Flow Help: Create & edit images](https://support.google.com/flow/answer/16729550?hl=en)
- Entry conditions: age verified as 18 or older, located in a supported region, a Chromium-based desktop browser recommended (Chrome or Edge), or the Flow mobile app (Android 12 or above, 2 GB RAM minimum). — READ DIRECTLY 17 Nov 2026: [Flow Help: Get started](https://support.google.com/flow/answer/16353333?hl=en); [Flow Help: Get started (Android view)](https://support.google.com/flow/answer/16353333?hl=en&co=GENIE.Platform%3DAndroid)
- Visible watermark: see section 4. In short, it is a setting, forced only in India, South Korea and Vietnam. — READ DIRECTLY 17 Nov 2026: [Flow Help: Get started](https://support.google.com/flow/answer/16353333?hl=en)
- In the Gemini app, a free user can generate images but not video: "To use this feature with a personal account, you must have a Google AI plan." — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: Generate videos](https://support.google.com/gemini/answer/16126339?hl=en)

### Inferences
- Clips per day on 50 credits (my arithmetic): 5 Veo 3.1 Lite clips of up to 8 s at 720p; or 2 Omni Flash 1.2 clips of 8 s at 720p (48 credits); or 6 Omni clips of 8 s at 360p (48 credits); or 3 Omni clips of 5 s at 720p (45 credits).
- Free users top out at 720p, because upscaling is for subscribers. A free 360p Omni clip cannot be upscaled inside Flow.
- For a European user the peak-hour window of 2 PM to 5 PM UTC falls in the afternoon and early evening (for example 4 PM to 7 PM in Sofia in winter), so free generation is best planned for mornings or late evenings.

### Gaps
- The page does not say in so many words that non-subscribers see the "Visible watermarking" switch; it only names a country exception. Confirm in the product.
- Queue speed for free users and how strict the peak-hour block is in practice.

## 4. Watermarks and provenance

### Takeaway
Every Flow and Gemini output carries an invisible SynthID watermark that cannot be switched off. The visible watermark is now an on/off user setting on all tiers, except in India, South Korea and Vietnam, where it is applied automatically unless the user is on the top Ultra plan. Gemini app output also carries C2PA Content Credentials.

### Cited Findings
- "All outputs generated in Google Flow using Veo, Omni, or Nano Banana include invisible SynthID watermarks." **Confirms and widens** the first-round third-party report (which covered only Omni Flash). — READ DIRECTLY 17 Nov 2026: [Flow Help: Get started](https://support.google.com/flow/answer/16353333?hl=en)
- "A visible watermark can be added to generated images and videos. You can control this with the 'Visible watermarking' toggle in the drop-down menu under your profile picture. A visible watermark will be applied automatically for users in India, South Korea, and Vietnam who are not on the Google One AI Ultra 20x Plan." **Makes the first-round lead (visible watermark below Ultra) out of date.** — READ DIRECTLY 17 Nov 2026: [Flow Help: Get started](https://support.google.com/flow/answer/16353333?hl=en)
- Flow's SynthID watermark "identifies the content as AI-generated and should not be tampered with or removed". — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage projects, assets & collections](https://support.google.com/flow/answer/16935308?hl=en)
- Gemini app: the setting is at Settings > Media Watermark and covers images, videos and music. In India, South Korea or Vietnam the setting is shown only to AI Ultra subscribers; everyone else there gets visible watermarks automatically. On video the visible mark is "a persistent overlay". — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: Manage watermark settings](https://support.google.com/gemini/answer/17405358?hl=en)
- Gemini app: "All AI-generated media created or edited with Gemini Apps includes an invisible SynthID watermark." "Gemini Apps include Content Credentials (C2PA) metadata." The visible-watermark setting "doesn't affect SynthID watermarks or Content Credentials". **New.** — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: Manage watermark settings](https://support.google.com/gemini/answer/17405358?hl=en)
- SynthID usually survives rescaling, recolouring and compression, "However, there's still a chance that after many alterations the watermark won't be detected." Anyone can check a file in the Gemini app (about 10 image, 10 video and 10 audio checks per 24 hours). — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: Verify AI-generated images, videos, and audio](https://support.google.com/gemini/answer/16722517?hl=en)
- Google announced the visible-watermark switch for Gemini and Flow on 14 August 2026; SynthID and C2PA stay in place when it is off. — SEARCH SUMMARY: [TechRepublic](https://www.techrepublic.com/article/news-google-gemini-visible-watermarks-optional/); [Gigazine, 17 Aug 2026](https://gigazine.net/gsc_news/en/20260817-google-visible-watermarks/); [TechRadar](https://techradar.com/ai-platforms-assistants/gemini/gemini-now-lets-you-turn-off-the-visible-watermark-on-your-ai-creations-heres-how-to-do-it-and-how-your-content-is-still-flagged-as-ai)
- Stale wording still on one Google page: the image-generation overview says Gemini uses "an invisible SynthID watermark, as well as a visible watermark". — READ DIRECTLY 17 Nov 2026: [gemini.google: image generation overview](https://gemini.google/overview/image-generation/)

### Inferences
- Outside India, South Korea and Vietnam, no plan tier forces a visible watermark any more, so paying does not "remove a watermark". The user should check that the switch is off before generating final clips.
- C2PA metadata matters downstream: YouTube says it may label content that contains C2PA metadata automatically and that such labels cannot be changed by the creator (section 10).

### Gaps
- The Flow help pages mention SynthID but not C2PA. Whether Flow downloads carry C2PA metadata is confirmed only by search coverage, not by a Google page I read.
- Whether the visible watermark is on or off by default for a new account.

## 5. Output specifications

### Takeaway
Flow generates at 360p or 720p, in landscape or portrait, with sound; clips run up to 8 s (Veo 3.1 Lite), 10 s (Omni Flash 1.2, free) or 15 s (Omni, subscribers). Subscribers can extend Omni clips by 3 to 10 s and upscale to 1080p (4K on Ultra). Reference images ("ingredients"), reusable characters, and first and last frame control are all supported.

### Cited Findings

**Resolution**
- Omni Flash 1.2 generates at 360p or 720p; Veo 3.1 Lite at 720p. Subscribers can "Upscale up to 1080p (or 4K for Ultra subscribers)". **Resolves the first-round conflict** between "720p only" and "upscales to 1080p or 4K": both are true, at different steps. — READ DIRECTLY 17 Nov 2026: [Flow Help: models & supported features](https://support.google.com/flow/answer/16352836?hl=en); [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- Downloads are offered as GIF (270p) or video files; uploads to YouTube go out "at the highest generated resolution available for your selected model". — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage projects, assets & collections](https://support.google.com/flow/answer/16935308?hl=en)

**Aspect ratio (vertical video)**
- Every video mode of Omni Flash 1.2 and Veo 3.1 Lite is listed with "Both aspect ratios", and the setting is called "Orientation". The help pages do not name the two ratios. — READ DIRECTLY 17 Nov 2026: [Flow Help: models & supported features](https://support.google.com/flow/answer/16352836?hl=en); [Flow Help: Edit videos & build scenes](https://support.google.com/flow/answer/16935718?hl=en)
- Veo 3.1 Lite supports landscape (16:9) and portrait (9:16). — SEARCH SUMMARY: [9to5Google, 31 March 2026](https://9to5google.com/2026/03/31/veo-3-1-lite/)
- Gemini app: "Choose the aspect ratio of the video before it's created"; the default for text prompts is landscape, and with an uploaded image or video the output matches the upload. — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: Generate videos](https://support.google.com/gemini/answer/16126339?hl=en)

**Audio**
- Flow generates sound by default: a failed audio track cancels the clip, and silent output is an opt-in project setting ("Return silent videos"). — READ DIRECTLY 17 Nov 2026: [Flow Help: Get started](https://support.google.com/flow/answer/16353333?hl=en); [Flow Help: Manage projects, assets & collections](https://support.google.com/flow/answer/16935308?hl=en)
- Omni Flash supports preset and custom voices as references, but "only to video generations that use ingredients". Google's Omni page lists "Native audio generation". — READ DIRECTLY 17 Nov 2026: [Flow Help: Create videos](https://support.google.com/flow/answer/16353334?hl=en); [gemini.google: Gemini Omni overview](https://gemini.google/overview/video-generation/)

**Clip length, extension and sequencing**
- Omni Flash 1.2: 3 to 10 s without a plan, 3 to 15 s with Plus, Pro or Ultra. Veo 3.1 Lite: 4, 6 or 8 s. **Confirms** the first round and adds the free-user limit. — READ DIRECTLY 17 Nov 2026: [Flow Help: models & supported features](https://support.google.com/flow/answer/16352836?hl=en)
- Omni Flash 1.2 generates 3 to 15 s in one-second steps. — SEARCH SUMMARY: [Google blog: Gemini Omni 1.2 Flash](https://blog.google/innovation-and-ai/technology/developers-tools/introducing-gemini-omni-1-2-flash/); [Android Authority](https://www.androidauthority.com/google-gemini-omni-1-2-flash-announced-3732209/)
- Extend ("Omni Extend"): "only available to Google AI Plus, Pro & Ultra subscribers on the Omni Flash 1.2 model", 3 to 10 s per extension, up to 3 image references, web only. Other edit modes cannot be applied to extended clips. Veo 3.1 Lite does not support extension. The first-round third-party claim of extension to 40 s in 10-s steps is **not confirmed**: no maximum total length is stated. — READ DIRECTLY 17 Nov 2026: [Flow Help: Edit videos & build scenes](https://support.google.com/flow/answer/16935718?hl=en); [Flow Help: models & supported features](https://support.google.com/flow/answer/16352836?hl=en)
- Scenebuilder arranges several clips in a sequence, reorders them, trims the start and end of each, previews the sequence and downloads it as one scene. Direct YouTube upload works only for single clips; a full sequence has to be downloaded first. — READ DIRECTLY 17 Nov 2026: [Flow Help: Edit videos & build scenes](https://support.google.com/flow/answer/16935718?hl=en); [Flow Help: Manage projects, assets & collections](https://support.google.com/flow/answer/16935308?hl=en)

**References and frame control**
- Veo 3.1 Lite supports Text to Video, "Frames to Video: First", "Frames to Video: First and last", and Ingredients/References to Video ("8s videos only"). It does not support video-to-video editing. **Answers the first-round gap** on first/last-frame and reference modes. — READ DIRECTLY 17 Nov 2026: [Flow Help: models & supported features](https://support.google.com/flow/answer/16352836?hl=en)
- Omni Flash 1.2 supports Text to Video, Frames to Video (web only), Ingredients/References to Video and Video to Video editing. Start and end frames are added by dragging images to "+ Add start frame" and "+ Add end frame". — READ DIRECTLY 17 Nov 2026: [Flow Help: models & supported features](https://support.google.com/flow/answer/16352836?hl=en); [Flow Help: Create videos](https://support.google.com/flow/answer/16353334?hl=en)
- Ingredients can be images or video; Google advises subject or product references "on a plain or segmented background". A reusable "character" bundles 1 or 2 images plus a voice and is called with @name. Any frame of a clip can be saved as an image and reused as an ingredient or as a start or end frame. — READ DIRECTLY 17 Nov 2026: [Flow Help: Create videos](https://support.google.com/flow/answer/16353334?hl=en); [Flow Help: Manage projects, assets & collections](https://support.google.com/flow/answer/16935308?hl=en); [Flow Help: Edit videos & build scenes](https://support.google.com/flow/answer/16935718?hl=en)
- Video-to-video editing (Omni only): upload up to 60 s and 1 GB (.mov, .mp4, .avi, .wmv), trim to 30 s, then edit a segment of up to 10 s (15 s for subscribers), with up to 3 follow-up turns. — READ DIRECTLY 17 Nov 2026: [Flow Help: Edit videos & build scenes](https://support.google.com/flow/answer/16935718?hl=en)

**Platform**
- Generation runs on Google's servers through a browser; Google recommends a desktop computer with a Chromium-based browser. The Flow Agent and Tools are "web & PC only". — READ DIRECTLY 17 Nov 2026: [Flow Help: Get started](https://support.google.com/flow/answer/16353333?hl=en); [Flow Help: Use the Google Flow Agent](https://support.google.com/flow/answer/17093911?hl=en)

### Inferences
- "Both aspect ratios" plus an "Orientation" setting, together with the 9to5Google report, makes 16:9 and 9:16 the two options with high probability. Native vertical 9:16 output for Reels, TikTok and Shorts is therefore available on both current models, but this is not stated in those words on a Google page I read.
- For 1080 x 1920 delivery, a subscriber can upscale Omni clips inside Flow at no credit cost. A free user, and possibly a Veo 3.1 Lite user, would deliver 720p or upscale elsewhere.
- A weak PC with integrated graphics is not a constraint for generation, since Flow only needs a Chromium browser.
- A workable 3D-style pipeline using only verified features: make a styled keyframe with Nano Banana in Flow (no credits), then animate it with Veo 3.1 Lite "Frames to Video: First" or first-and-last frames (10 credits), keeping a reusable character for consistency.

### Gaps
- Exact aspect ratios, frame rate, bitrate and container format are not on the help pages.
- Maximum number of ingredient images per generation in Flow (the Gemini app allows one video and up to 5 images).
- Maximum total length after repeated extensions.
- Whether Veo 3.1 Lite output can be upscaled (see section 1).

## 6. Announced changes: the 5 December 2026 retirement

### Takeaway
It is true: on 5 December 2026 Flow retires Veo 3.1 Fast, Veo 3.1 Quality and Omni Flash 1.1, and Google tells users to move to Omni Flash 1.2 or Veo 3.1 Lite. The surviving models keep their listed rates, but the cheapest-per-clip Omni option disappears, so an 8-second 720p Omni clip goes from 12 credits (version 1.1) to 24 credits (version 1.2).

### Cited Findings
- "On December 5, 2026, Veo 3.1 Fast, Veo 3.1 Quality, and Omni Flash 1.1 will be retired. Until then, you can generate with these models at standard credit rates while transitioning your workflows to Omni Flash 1.2 or Veo 3.1 Lite." **Confirms.** — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- The models page repeats the date and adds "we recommend switching to Omni Flash 1.2 or Veo 3.1 Lite for future projects". — READ DIRECTLY 17 Nov 2026: [Flow Help: models & supported features](https://support.google.com/flow/answer/16352836?hl=en)
- "On November 5, 2026, Veo Extend was retired. To extend a video, you must be a Google AI Plus, Pro, or Ultra subscriber and use Omni Flash 1.2." **New.** — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- "Gemini Omni will replace Veo in the Gemini app." **Confirms** the first-round third-party report. — READ DIRECTLY 17 Nov 2026: [gemini.google: Gemini Omni overview](https://gemini.google/overview/video-generation/)
- Omni 1.2 Flash was released on 5 November 2026, raising the maximum clip from 10 to 15 s. **Consistent with** the first-round date. — SEARCH SUMMARY: [Google blog: Gemini Omni 1.2 Flash](https://blog.google/innovation-and-ai/technology/developers-tools/introducing-gemini-omni-1-2-flash/); [Let's Data Science](https://letsdatascience.com/news/google-launches-gemini-omni-12-flash-with-15-second-video-ch-678ef595)
- Veo 3.1 Quality is the only listed model without Ingredients support; Veo 3.1 Fast and Quality support first and last frames, as Lite does. — READ DIRECTLY 17 Nov 2026: [Flow Help: models & supported features](https://support.google.com/flow/answer/16352836?hl=en)
- Flow itself has moved: `labs.google/fx` now says "Looking for Google Flow or Google Flow Music? Find them at their dedicated sites: flow.google and flowmusic.google!", and `labs.google/fx/tools/flow` and `labs.google/fx/tools/whisk` answer with a redirect to `flow.google.com` (the Whisk address redirects to `flow.google.com/?from=whisk`). **New; the first-round link to the Flow page on labs.google no longer resolves there.** — READ DIRECTLY 17 Nov 2026: [labs.google/fx](https://labs.google/fx)
- Some Google pages still carry older wording: the subscriptions FAQ mentions "a limited trial of Veo 3.1 Lite" for Pro and "video generation with Veo 3.1" for Ultra, and the AI Pro benefits list says "Gemini app with Gemini 4 Argon and Veo". — READ DIRECTLY 17 Nov 2026: [Gemini subscriptions page (US)](https://gemini.google/subscriptions/); [Google One Help: Use Google AI Pro benefits](https://support.google.com/googleone/answer/14534406?hl=en)

### Inferences
- What an 8-second clip costs before and after 5 December 2026 (credits, non-Ultra; from the tables in section 1):

| Option | Until 5 Dec 2026 | From 5 Dec 2026 |
|---|---|---|
| Veo 3.1 Lite, 720p | 10 | 10 |
| Veo 3.1 Fast, 720p | 20 | retired |
| Veo 3.1 Quality | 100 | retired |
| Omni Flash 1.1, 720p / 360p | 12 / 6 | retired |
| Omni Flash 1.2, 720p / 360p | 24 / 8 | 24 / 8 |
| Edit a clip (8 s, 720p) | 40 (Omni 1.1) or 24 (Omni 1.2) | 24 |

- Google's pages announce no change to the rates of the two surviving models. The effective change is the loss of options: no higher-quality Veo tier in Flow, and Omni generation at 720p costs twice what version 1.1 cost for an 8-second clip. Short edits get cheaper (per-second pricing replaces the flat 40 credits).
- Reviews that rate "Veo 3.1" best overall usually tested the Fast or Quality tier. From 5 December those tiers are gone from Flow, so the user should judge Veo 3.1 Lite and Omni Flash 1.2 on their own test clips.
- With three Omni Flash versions and two retirements inside one year, any workflow or price in this file may change again. Re-check the Flow credits page before committing to a plan.

### Gaps
- Whether Veo 3.1 Fast and Quality stay available outside Flow (API, Vertex AI) after 5 December. I could not open the Gemini API pricing page; see section 11 for the search-summary figures.
- No Google page I read mentions a Veo 4 or a successor to Veo 3.1 Lite.

## 7. Gemini app: video and image generation limits per plan

### Takeaway
In the Gemini app, video generation uses Gemini Omni 1.2 Flash and is only for paying subscribers aged 18 or over; Google publishes no number of videos per day, only a compute-based allowance that refreshes every 5 hours up to a weekly cap. Image generation with Nano Banana is free for everyone, with a better model and "Redo with Pro" on paid plans, but the live help page gives no numeric daily image limit.

### Cited Findings

**Video**
- "You can create videos or animated GIFs in minutes in Gemini Apps with Gemini Omni 1.2 Flash, our latest AI video generation model." **Confirms** the first-round third-party reports. — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: Generate videos](https://support.google.com/gemini/answer/16126339?hl=en)
- Requirements: a Google AI plan (personal accounts); "this feature isn't available to users under 18". The marketing page says "Google AI subscription required. Features vary by tier and geography. 18+." **Answers the first-round gap: no free video in the Gemini app.** — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: Generate videos](https://support.google.com/gemini/answer/16126339?hl=en); [gemini.google: Gemini Omni overview](https://gemini.google/overview/video-generation/)
- The feature table marks "Video generation" with a check mark for AI Plus, AI Pro and AI Ultra and with a different, unlabelled icon for "Without a Google AI plan". "Image generation with Nano Banana 2" and "Music generation" have check marks in all four columns; "Redo images with Nano Banana Pro" only in the three paid columns. — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: limits & feature availability](https://support.google.com/gemini/answer/16275805?hl=en)
- Video length: "from 3 seconds to up to 10 seconds long or up to 15 seconds for users with an AI Ultra subscription". Note the difference from Flow, where Plus and Pro also get 15 s. — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: Generate videos](https://support.google.com/gemini/answer/16126339?hl=en)
- Inputs and editing: one video and up to 5 images per request; multi-turn editing in one conversation; "Extend the video length up to another 10 seconds"; audio on request; download or "Share on YouTube". Generation "may take a few minutes". — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: Generate videos](https://support.google.com/gemini/answer/16126339?hl=en)
- Limits: "Gemini Apps have compute-based usage limits... Your limit refreshes every 5 hours until you reach your weekly limit." Without a plan: standard limits; AI Plus: 2x; AI Pro: 4x; AI Ultra: 5x or 20x the AI Pro limits. Video generation is rated "High" usage: "Video generally requires the most usage." No count of videos is given. **Confirms.** — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: limits & feature availability](https://support.google.com/gemini/answer/16275805?hl=en)
- When a subscriber hits the limit, chat continues on the Flash-Lite model until the limit refreshes. Usage can be viewed at Settings > Usage Limits. — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: limits & feature availability](https://support.google.com/gemini/answer/16275805?hl=en)
- Can AI credits extend Gemini app limits? The subscriptions page footnote says "You can extend your limits by purchasing AI credits", but the Google One pages describe AI credits as extra usage "in Google Flow and Google Antigravity", and the Gemini limits page mentions only upgrading or waiting. Unresolved conflict between Google pages. — READ DIRECTLY 17 Nov 2026: [Gemini subscriptions page (US)](https://gemini.google/subscriptions/); [Google One Help: Manage your AI credits](https://support.google.com/googleone/answer/16287445?hl=en)
- No per-day video count and no tested "videos per allowance" figure was found by search either. One May 2026 plan comparison listed Omni Flash video under the Free tier, which **conflicts** with the Google pages read today. — SEARCH SUMMARY: [9to5Google, 25 May 2026](https://9to5google.com/2026/05/25/google-ai-plus-pro-ultra-gemini-features/)

**Images (Nano Banana versions)**
- Help-centre naming: "Nano Banana Lite" (used when the Gemini model is Flash-Lite), "Nano Banana 2" (when the model is Flash or Pro; accepts multiple reference images) and "Nano Banana Pro 2" (used through "Redo with Pro"; needs a Google AI plan). — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: Generate & edit images](https://support.google.com/gemini/answer/14286560?hl=en)
- Marketing-page naming: "Nano Banana 2" is "Free"; "Nano Banana 2.1", "our best image generation and editing model", comes "With a Google AI plan"; both list "2K resolution"; paid plans get "higher generation limits". Paid users "can regenerate images using Nano Banana Pro". — READ DIRECTLY 17 Nov 2026: [gemini.google: image generation overview](https://gemini.google/overview/image-generation/)
- A daily image quota exists ("If you reach your daily quota of Nano Banana 2 images, you can't redo any additional images with Nano Banana Pro") but the live pages state no number. I checked the English, UK English, German and Bulgarian versions of the limits page; none has a numeric image limit. — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: Generate & edit images](https://support.google.com/gemini/answer/14286560?hl=en); [Gemini Apps Help: limits & feature availability](https://support.google.com/gemini/answer/16275805?hl=en)
- Older figures of up to 20 images a day (free), 50 (AI Plus), 100 (AI Pro) and 1,000 (AI Ultra) are attributed to an earlier version of Google's limits page. They are **not on the live page** and probably predate the move to compute-based limits. — SEARCH SUMMARY: [Gemini Apps Help: limits (search-indexed older version)](https://support.google.com/gemini/answer/16275805?hl=en-GB)
- Age rules: generating images needs age 13 or over; editing images needs 18 or over. — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: Generate & edit images](https://support.google.com/gemini/answer/14286560?hl=en)

### Inferences
- The Gemini app allowance appears to be separate from Flow credits: the Flow pages describe credits as what you need "to generate content in Google Flow", and the Gemini pages describe a compute allowance. If so, an AI Plus subscriber gets Omni clips in the Gemini app on top of the Flow credits. Google does not state this in one sentence, so treat it as likely, not confirmed.
- Because the size of the Gemini app allowance is unpublished, no cost per clip can be computed for it. For planning and budgeting, Flow is the only Google surface with countable costs.
- For keyframes, Flow is the better-documented free route (published daily limits and a choice of three models) than the Gemini app (no published number).

### Gaps
- Number of Omni videos an AI Plus or AI Pro subscriber can make per 5 hours or per week.
- Current numeric image limits in the Gemini app.
- Output resolution of Gemini app videos (not stated on the help page).
- Google's naming is inconsistent between its own pages (Nano Banana Lite / 2 / Pro 2 in the Gemini help centre; Nano Banana 2 / 2.1 / Pro on the marketing page; Nano Banana 2 Lite / 2.1 / Pro in Flow).

## 8. Country availability (Flow and Gemini app video), with EU/EEA and UK status

### Takeaway
Flow is officially available to adults in 152 listed countries and territories, including all 27 EU member states, Iceland, Liechtenstein, Norway, Switzerland and the United Kingdom. In the EEA, Switzerland and the UK two features are switched off: editing uploaded videos, and avatars. The Gemini app's video generation follows the paid plans, which are sold in all of those countries too.

### Cited Findings
- Flow's supported-countries table has 152 entries (my count) and includes every EU member state (Austria, Belgium, Bulgaria, Croatia, Cyprus, Czechia, Denmark, Estonia, Finland, France, Germany, Greece, Hungary, Ireland, Italy, Latvia, Lithuania, Luxembourg, Malta, Netherlands, Poland, Portugal, Romania, Slovakia, Slovenia, Spain, Sweden), plus Iceland, Liechtenstein, Norway, Switzerland, the United Kingdom and the United States. The same list applies to the desktop site and the mobile app. **Answers the first-round gap.** — READ DIRECTLY 17 Nov 2026: [Flow Help: Where you can use Google Flow](https://support.google.com/flow/answer/16353544?hl=en)
- "Editing of uploaded videos is currently not supported in" the European Economic Area, Switzerland and the United Kingdom. Avatars are also unavailable there. **New.** — READ DIRECTLY 17 Nov 2026: [Flow Help: Where you can use Google Flow](https://support.google.com/flow/answer/16353544?hl=en); [Flow Help: Create & use your avatar](https://support.google.com/flow/answer/17102997?hl=en)
- Not supported in any region: editing uploaded videos of identifiable minors, generating videos of prominent people, and editing or generating what people say in uploaded videos (dubbing, new dialogue). — READ DIRECTLY 17 Nov 2026: [Flow Help: Where you can use Google Flow](https://support.google.com/flow/answer/16353544?hl=en)
- Access rules: age 18 or over with age verified; "VPNs will not enable access in unsupported regions"; "Google Flow is not currently available in all countries where Google AI Pro is offered"; buying AI credits is unavailable in Japan. — READ DIRECTLY 17 Nov 2026: [Flow Help: Get started](https://support.google.com/flow/answer/16353333?hl=en); [Flow Help: Where you can use Google Flow](https://support.google.com/flow/answer/16353544?hl=en)
- Flow's interface supports 86 listed languages, including Bulgarian; "we recommend using English prompts". — READ DIRECTLY 17 Nov 2026: [Flow Help: Where you can use Google Flow](https://support.google.com/flow/answer/16353544?hl=en)
- Paid plans: the AI Plus list has 168 entries and the AI Pro and Ultra list 161 entries (my counts); both include all EU and EEA states, Switzerland, the UK and the US. The plans page says Plus is in "more than 160 countries and territories" and Pro and Ultra in "more than 150". — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: limits & feature availability](https://support.google.com/gemini/answer/16275805?hl=en); [Gemini subscriptions page (US)](https://gemini.google/subscriptions/)
- Gemini web app: "more than 70 languages and over 230 countries and territories". Gemini mobile apps: "more than 150 countries". — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: Where you can use the Gemini web app](https://support.google.com/gemini/answer/13575153?hl=en); [Gemini Apps Help: Gemini mobile app availability](https://support.google.com/gemini/answer/14579026?hl=en)
- Gemini app video in Europe: "Uploading videos to use for video edits and avatar creation and sharing aren't available in the EEA, Switzerland, the United Kingdom, and some US states." GIF creation works only in Australia, Canada, France, Germany, Japan, Korea, the UK and the US. In the EEA, Switzerland or the UK a user must be 18 or over to use Gemini Apps with a Google AI plan. — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: Generate videos](https://support.google.com/gemini/answer/16126339?hl=en); [Gemini Apps Help: limits & feature availability](https://support.google.com/gemini/answer/16275805?hl=en)
- AI image generation in the Gemini app "is available in all languages and countries where the Gemini app is available". — READ DIRECTLY 17 Nov 2026: [gemini.google: image generation overview](https://gemini.google/overview/image-generation/)

### Inferences
- For a creator in the EU, EEA or UK, the core workflow (text, frames and ingredients to video with Veo 3.1 Lite and Omni Flash 1.2, plus Nano Banana images) is available. What is missing is the ability to restyle or edit their own uploaded footage with Omni and to use a personal avatar. Editing clips that Flow itself generated is not named in the restriction.
- Because Flow is "not available in all countries where Google AI Pro is offered", a buyer should check the Flow list first and the plan list second.

### Gaps
- Google publishes no separate country list for video generation in the Gemini app. Availability is implied by plan availability plus the stated exceptions.
- Whether "some Omni features and voice customizations... only available in certain regions" affects custom voices in the EEA or UK. The page does not list which features.

## 9. Usage rights: commercial use and ownership

### Takeaway
Google's help pages do not tie commercial use to a paid plan: they point to the Google Terms of Service and quote them as saying Google "won't claim ownership" of content you generate. The user remains responsible for what they publish, must follow the Prohibited Use Policy, and should not tamper with SynthID.

### Cited Findings
- Flow FAQ, "Can I use outputs of these tools for commercial purposes?": "The Terms of Service govern how these tools may be used, and must be consulted and followed in their entirety. Per those terms: Some of our services allow you to generate original content. Google won't claim ownership over that content". **Answers the first-round gap** for Google. The same wording is on the labs.google FAQ. — READ DIRECTLY 17 Nov 2026: [Flow Help: Get started](https://support.google.com/flow/answer/16353333?hl=en); [labs.google/fx FAQ](https://labs.google/fx/faq)
- No Flow or Gemini help page read makes commercial use depend on the plan tier. By contrast, the Flow Music benefit explicitly lists "Commercial use rights" for the plans bundled with AI Plus (Starter, 3,000 monthly music credits) and AI Pro (Plus, 10,000 monthly music credits). — READ DIRECTLY 17 Nov 2026: [Google One Help: Use Google AI Plus benefits](https://support.google.com/googleone/answer/16882689?hl=en); [Google One Help: Use Google AI Pro benefits](https://support.google.com/googleone/answer/14534406?hl=en)
- Gemini app video: users "agreed to Google's Terms of Service, including the Prohibited Use Policy. You must have rights to any images that you upload. Be sure not to violate others' rights, including copyright or privacy rights... Use your discretion before you rely on, publish, or use videos that Gemini Apps generate." The image page carries the same warning. — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: Generate videos](https://support.google.com/gemini/answer/16126339?hl=en); [Gemini Apps Help: Generate & edit images](https://support.google.com/gemini/answer/14286560?hl=en)
- Gemini Apps User Guidelines apply both to generating and to distributing content, and include: "Do not use Gemini Apps to enable or create automated or repetitive commercial or promotional content (spam)." — READ DIRECTLY 17 Nov 2026: [Gemini Apps Help: User Guidelines](https://support.google.com/gemini/answer/18481641?hl=en)
- Data use: with "Help improve Google Flow" on, Google may use interactions, uploads and generated output to improve its products and models; human reviewers see some interactions, which are kept up to 18 months; the setting can be turned off. Sharing a Flow link means "anyone with the link can find and use your creation". — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your data](https://support.google.com/flow/answer/17025472?hl=en); [Flow Help: Manage projects, assets & collections](https://support.google.com/flow/answer/16935308?hl=en)
- The Google Terms of Service contain the clause "Some of our services allow you to generate original content. Google won't claim ownership over that content"; Google's example at the time was that a Gemini-generated poem could be published in a book without a licence from Google. Google's API terms add that Google may generate the same or similar content for others, and Google's terms bar using generated output to develop machine-learning models. — SEARCH SUMMARY: [Google Terms of Service](https://policies.google.com/terms); [9to5Google, 16 April 2024](https://9to5google.com/2024/04/16/google-tos-ai/); [Gemini API terms preview](https://ai.google.dev/gemini-api/terms_preview)

### Inferences
- On the pages read, a free user and a paying user are in the same position on rights: Google does not claim ownership in either case, and no page reserves commercial use for subscribers.
- "Google won't claim ownership" is not the same as a guarantee that the output is protected by copyright or free of third-party claims. Those risks stay with the creator, as the help pages' warnings indicate.
- The spam clause targets deceptive or mass promotional content. A creator publishing original, varied social videos is not the stated target, but high-volume templated promotional posting could fall under it.

### Gaps
- I could not read `policies.google.com` directly, so the exact current text of the Terms of Service and of the Generative AI Prohibited Use Policy is from a search summary.
- No statement on indemnity for consumer plans was found.
- Rules on logos, brand characters and copyrighted characters beyond the general "don't violate others' rights" wording were not found on the pages read.

## 10. YouTube: disclosure of AI content and monetisation wording

### Takeaway
YouTube requires disclosure only for AI-generated or altered content that looks realistic; clearly non-realistic or animated content does not need it, and disclosure alone does not reduce reach or earnings. Monetisation rules exclude content that is "mass-produced, generic, repetitive, or manipulative", and name templated AI content as an example.

### Cited Findings

**Disclosure (page now titled "Disclosing use of GenAI content")**
- "We require creators to disclose AI-generated or altered content that seems realistic." Disclosure is required for content that makes a real person appear to say or do something they did not, alters footage of a real event or place, generates "a realistic scene that didn't actually occur", or creates music that is the main focus of the video. — READ DIRECTLY 17 Nov 2026: [YouTube Help: Disclosing use of GenAI content](https://support.google.com/youtube/answer/14328491?hl=en)
- Not required: "non-realistic content that's made with AI" (examples: "Someone riding a unicorn through a fantastical world"; "an AI-generated or altered animation of a missile in a fully animated video"), minor edits, and production help such as AI-made outlines, scripts, thumbnails, titles, captions and upscaling. — READ DIRECTLY 17 Nov 2026: [YouTube Help: Disclosing use of GenAI content](https://support.google.com/youtube/answer/14328491?hl=en)
- How: in YouTube Studio, in the upload's Attributes section, under "AI use", select Yes or No. — READ DIRECTLY 17 Nov 2026: [YouTube Help: Disclosing use of GenAI content](https://support.google.com/youtube/answer/14328491?hl=en)
- Labels: a label on the video player "for AI-generated music or content that is photorealistic"; a label in the expanded description for "AI content that is non-photorealistic or animated". "Disclosing AI content alone won't limit a video's audience or impact its eligibility to earn money." — READ DIRECTLY 17 Nov 2026: [YouTube Help: Disclosing use of GenAI content](https://support.google.com/youtube/answer/14328491?hl=en)
- Automatic labels: YouTube "may automatically apply an AI label" for content made with YouTube's own GenAI tools, "Content that contains C2PA metadata", and content its systems detect as AI generated or altered. Creators can usually correct an error, but labels on content "containing C2PA metadata" "can not be adjusted". — READ DIRECTLY 17 Nov 2026: [YouTube Help: Disclosing use of GenAI content](https://support.google.com/youtube/answer/14328491?hl=en)
- Risk of not disclosing: creators who "consistently choose not to disclose" may get labels applied manually or face "removal of content or suspension from the YouTube Partner Program". — READ DIRECTLY 17 Nov 2026: [YouTube Help: Disclosing use of GenAI content](https://support.google.com/youtube/answer/14328491?hl=en)

**Monetisation policy wording**
- Standing notice on the page: on 15 July 2025 YouTube updated the "repetitious content" policy "to better clarify this includes content that is repetitive or mass-produced" and renamed it "inauthentic content". "This type of content has always been ineligible for monetization." — READ DIRECTLY 17 Nov 2026: [YouTube Help: channel monetization policies](https://support.google.com/youtube/answer/1311392?hl=en)
- Current core test: monetised content should "Be your original creation" and "Not be mass-produced, generic, repetitive, or manipulative. It should be made for the enjoyment or education of viewers, rather than for the sole purpose of getting views." — READ DIRECTLY 17 Nov 2026: [YouTube Help: channel monetization policies](https://support.google.com/youtube/answer/1311392?hl=en)
- The body section is now headed "Generic or Repetitive Content". Not allowed to monetise, among other examples: "AI-generated content made with generic or unoriginal templates giving the impression of mass production without adding the creator's original, authentic insights or perspective" and "Image slideshows, templated storylines, or scrolling text with minimal or no narrative, commentary, or educational value". Allowed: the same intro and outro with different main content, or a series with recurring characters where "each video has a distinct storyline, focus, or concept". — READ DIRECTLY 17 Nov 2026: [YouTube Help: channel monetization policies](https://support.google.com/youtube/answer/1311392?hl=en)
- A further section, "Unsatisfying or Off-putting Content", allows "using AI to visualize a unique character and narrative you invented" and using AI to "generate a unique background visual", and excludes "videos that stitch together unrelated or inconsistent AI clips to surprise or shock viewers". If automated tools or templates are used, "the final product must still demonstrate your creative vision". — READ DIRECTLY 17 Nov 2026: [YouTube Help: channel monetization policies](https://support.google.com/youtube/answer/1311392?hl=en)
- A separate rule bars monetisation of channels that use AI personas presented as human experts on health, legal, financial or political topics. — READ DIRECTLY 17 Nov 2026: [YouTube Help: channel monetization policies](https://support.google.com/youtube/answer/1311392?hl=en)
- Partner Programme thresholds: 1,000 subscribers plus either 4,000 qualified watch hours in 12 months or 10 million qualified Shorts views in 90 days. Updated terms take effect on 1 February 2027 and must be accepted by 31 January 2027. — READ DIRECTLY 17 Nov 2026: [YouTube Help: YouTube Partner Program overview & eligibility](https://support.google.com/youtube/answer/72851?hl=en)
- Shorts: "Starting February 1, 2027, to be eligible to earn a share of Shorts ad revenue... for each month, you will need to have at least 10 million qualified Shorts views in the last 90 days." Views of "non-original Shorts" (unedited clips, re-uploads, compilations with nothing added) are not counted for payment. — READ DIRECTLY 17 Nov 2026: [YouTube Help: Shorts monetization policies](https://support.google.com/youtube/answer/12504220?hl=en)

### Inferences
- A stylised 3D-animation Short that could not be mistaken for real footage does not need the "AI use" disclosure under the wording above. A photorealistic product render or realistic scene would.
- Clips made in the Gemini app carry C2PA metadata, so YouTube may label them as AI automatically and the creator cannot remove that label. For animated content the label sits in the expanded description. This has no stated effect on reach or earnings.
- The monetisation risk for this user is not the use of AI as such but volume without variety: a channel of near-identical templated clips fits the "mass production" example. A recurring character with a distinct idea per video fits the "allowed" examples.
- From 1 February 2027 Shorts ad revenue needs 10 million qualified Shorts views every rolling 90 days, which is a high bar for a new solo creator. YouTube Shorts income should not be assumed in a cost-recovery plan.

### Gaps
- Rules for X, Instagram and TikTok are outside this file (another researcher covers platform rules).
- Whether Flow downloads carry the C2PA metadata that triggers YouTube's automatic label (see section 4 Gaps).
- The detailed content of the YouTube Partner Programme terms that take effect on 1 February 2027 was not on the pages read.

## 11. Verified cost of one 8-second clip and one finished 30-second video

### Takeaway
On verified figures, one 8-second 720p clip costs 10 credits with Veo 3.1 Lite or 24 credits with Omni Flash 1.2: nothing for a free user (within 50 credits a day), about $0.25 or $0.60 on AI Plus, and about $0.20 or $0.48 on AI Pro. A finished 30-second video (12 generations) costs $0 and about 3 days of daily credits for a free user with Veo 3.1 Lite, about $2.99 (Lite) or $7.19 (Omni 720p) on AI Plus, and about $2.40 or $5.76 on AI Pro; the first-round dollar figures were right.

### Cited Findings
Verified inputs used below (all restated from sections 1 and 2):
- Veo 3.1 Lite: 10 credits per 4, 6 or 8 s clip at 720p for non-Ultra users. Omni Flash 1.2: 1 credit per second at 360p and 3 credits per second at 720p, up to 10 s, for all users. Subscribers upscale clips of up to 10 s to 720p or 1080p for 0 credits. — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- 50 daily credits for everyone; monthly credits of 200 (AI Plus) and 1,000 (AI Pro); no rollover. — READ DIRECTLY 17 Nov 2026: [Flow Help: Manage your Google Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- US prices: AI Plus $4.99 and AI Pro $19.99 a month. — READ DIRECTLY 17 Nov 2026: [Gemini subscriptions page (US)](https://gemini.google/subscriptions/)
- Top-up credits at $25 per 2,500 (Pro and Ultra only). — SEARCH SUMMARY: [Google One Help: Purchase Google AI credits (search-indexed version)](https://support.google.com/googleone/answer/17103110?hl=en-MY)
- Gemini API comparison prices: Gemini Omni 1.2 Flash at $0.07 per second at 720p (announced 5 November 2026, a 30% cut); Veo 3.1 Lite listed at $0.05 per second at 720p in a September 2026 snapshot, with one source saying the Veo 3.1 Preview line was shut down on 22 October 2026. I could not open Google's API pricing page, so the first-round API table remains unverified. — SEARCH SUMMARY: [FourWeekMBA](https://fourweekmba.com/ai-google-cuts-gemini-omni-video-price-30-to-0-07-a-second/); [Tech Insider](https://tech-insider.org/gemini-omni-1-2-flash-15-second-video-30-percent-price-cut-2026/); [benchlm.ai](https://benchlm.ai/media-pricing/veo)

### Inferences
Everything in this subsection is my arithmetic on the verified inputs above.

**Assumption (stated as requested):** one finished 30-second video = 4 shots of 8 seconds, with 3 generations per usable shot = **12 generations of 8 seconds**. The 4 kept shots give 32 seconds, trimmed to 30. Subscription credits are valued at plan price divided by monthly credits (AI Plus $0.02495, AI Pro $0.01999 per credit). This ignores the free daily credits, the other benefits of the plan, tax, music and editing.

**Credits needed**

| | Veo 3.1 Lite, 720p | Omni Flash 1.2, 720p | Omni Flash 1.2, 360p |
|---|---|---|---|
| One 8-second clip | 10 credits | 24 credits | 8 credits |
| Finished 30-second video (12 generations) | 120 credits | 288 credits | 96 credits |
| Getting to 1080p | Not confirmed for Lite | Subscribers: 0 credits per clip | Subscribers: 0 credits per clip. Free users: not possible in Flow |

**Cost per plan**

| Plan (US, monthly) | 8-s clip, Veo 3.1 Lite | 8-s clip, Omni 720p | 8-s clip, Omni 360p | Finished video, Veo 3.1 Lite | Finished video, Omni 720p | Finished video, Omni 360p |
|---|---|---|---|---|---|---|
| Free ($0; 50 credits a day) | $0 (uses 10 of the day's 50) | $0 (uses 24 of 50) | $0 (uses 8 of 50) | $0; 2.4 days of credits, so 3 calendar days | $0; 6 days | $0; 2 days, 360p output only |
| AI Plus ($4.99; 200 monthly credits) | $0.25 | $0.60 | $0.20 | $2.99 | $7.19 | $2.40 |
| AI Pro ($19.99; 1,000 monthly credits) | $0.20 | $0.48 | $0.16 | $2.40 | $5.76 | $1.92 |

- These match the first-round table for AI Plus at $4.99 and AI Pro. The first-round row "AI Plus at $7.99" should be dropped (wrong price for the US). The Omni 360p column and the free-user row are new.
- For subscribers, the Omni 360p column includes a free upscale of the kept shots to 1080p. It is the cheapest verified way to a 1080p file inside Flow, at $1.92 per finished video on AI Pro. How good an upscaled 360p clip looks was not tested.

**How many finished videos the allowance covers**

| Plan | From monthly credits alone: Veo 3.1 Lite | Omni 720p | Omni 360p | Adding the 50 daily credits, used every day for 30 days: Veo 3.1 Lite | Omni 720p | Omni 360p |
|---|---|---|---|---|---|---|
| Free | none (no monthly credits) | none | none | 12 (150 clips) | 5 (60 clips) | 15 (180 clips, 360p only) |
| AI Plus (200) | 1 (1.67; 20 clips) | 0 (0.69; 8 clips) | 2 (2.08; 25 clips) | 14 (170 clips) | 5 (about 68 clips) | 17 (about 205 clips) |
| AI Pro (1,000) | 8 (8.33; 100 clips) | 3 (3.47; 41 clips) | 10 (10.4; 125 clips) | 20 (250 clips) | 8 (about 101 clips) | 25 (about 305 clips) |

- The daily-credit columns are an upper bound. They assume the user generates every single day (unused daily credits are lost) and, for a free user, is not blocked at peak hours. Whole clips are counted per day: 5 Lite clips, 2 Omni 720p clips or 6 Omni 360p clips fit into 50 credits.
- AI Plus cannot cover even one Omni 720p video from its 200 monthly credits (288 needed). It needs the daily credits as well.
- **Confirms** the first-round capacity line for AI Pro ("about 8 finished 30-s videos per month, or about 3.5 with Omni Flash at 720p").

**Other verified price points**
- Top-up route (AI Pro or Ultra only, if the search-summary price of $0.01 per credit still holds): $0.10 per Veo 3.1 Lite clip, $0.24 per Omni 720p clip, $0.08 per Omni 360p clip; a finished video costs $1.20, $2.88 or $0.96. Top-up credits are half the price of AI Pro's bundled credits, but the smallest pack is $25.
- Until 5 December 2026 only, on AI Pro: Omni Flash 1.1 at 720p is $0.24 per 8-s clip and $2.88 per finished video; Veo 3.1 Fast is $0.40 and $4.80; Veo 3.1 Quality is $2.00 per clip, and a finished video needs 1,200 credits ($23.99), more than the whole monthly allowance.
- AI Ultra for reference: Veo 3.1 Lite costs 5 credits, so $0.05 per clip and $0.60 per finished video on the $99.99 tier.
- Per-second view at 720p: Omni Flash 1.2 in Flow costs about $0.06 per second on AI Pro credits and $0.075 on AI Plus credits, against $0.07 per second on the Gemini API (search summary). Veo 3.1 Lite in Flow costs about $0.025 per second for an 8-second clip on AI Pro.
- Sensitivity: the 12-generation assumption drives every figure. One generation per shot cuts costs to a third; five per shot raises them by two thirds.
- Stills: keyframes made with Nano Banana inside Flow add $0, within the daily image limits in section 1.

**What this means for the end user (inference, for the report writer to weigh)**
- The lowest-cost verified route is a free Flow account with Veo 3.1 Lite: 5 clips a day at 720p with sound, in either orientation, no forced visible watermark outside three Asian countries, and free keyframes. One finished 30-second video takes about three days of allowance and no money.
- AI Plus at $4.99 does not add many credits (200, worth 20 Lite clips). What it buys is the removal of the peak-hour block, 15-second Omni clips, Extend, free upscaling to 1080p, more Nano Banana Pro images (100 a day against 20), and Omni video in the Gemini app. For a creator who needs 1080p files, that is the cheapest verified step up.
- AI Pro at $19.99 makes sense when the user wants to produce several videos in a few days: its 1,000 credits cover 8 Lite videos or 10 Omni-360p-upscaled videos without waiting for daily refreshes, and it is the cheapest plan that can buy top-ups.

### Gaps
- The order in which daily and monthly credits are spent is unknown, which slightly affects the "with daily credits" counts for subscribers.
- The real number of generations per usable shot for stylised 3D looks is untested; 3 is an assumption carried over from the first round.
- The Gemini app's video allowance cannot be costed because Google publishes no quantity.
- Gemini API prices could not be read directly; the first-round API table is neither confirmed nor corrected here.
- Quality of Veo 3.1 Lite and Omni Flash 1.2 for Pixar-like, clay, toy or isometric looks is not addressed by any Google page read. It needs a hands-on test, which the free daily credits allow at no cost.
