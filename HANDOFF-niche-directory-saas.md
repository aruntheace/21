# Handoff: Niche "near me" directories + vertical micro-SaaS

**From:** cloud session `session_01LDN9WHRPQ1MaTTTPjFe1Ss` ("Niche directory and SaaS opportunities"), started from iOS on 2026-11-09.
**Written:** 2026-11-10.
**Repo:** `aruntheace/21`. Research lives on branch `claude/jolly-babbage-e38so9`. This handoff is on `handoff/niche-directory-saas`, which branches from it, so all files below are present here too.

---

## 1. What Arun wants

### The goal
- Find **"near me" local-service segments** where he can build a **directory site** from data scraped and collected from **Google Business Profile** listings.
- Build **micro-SaaS for the same businesses** alongside each directory. The directory doubles as the lead list (claim-your-listing leads to a software upsell).
- **Target:** segments that are **not super competitive** (he gave "dentist near me" as the counter-example), small enough that a couple of players exist, but where **$5–10K MRR from SaaS** is realistic.
- **Existing work:** he already runs or is building a **dumpster rental directory** (Miami named as the example; the "Dumpelo" name appears in his other session titles). Synergy with that counts as a plus.
- He is fine with data mining and scraping.

### How he likes to work
- **Use the Ahrefs API, carefully.** Units were nearly exhausted this cycle.
- **Don't download whole datasets.** He pushed back hard on pulling a year of Reddit data through a cloud container. Queries must run **next to the data** and bring back only matches.
- He works from both phone and laptop, and expects things to happen without many manual steps.
- He wanted far more segments than the first round found. Lead with **clusters, volume, CPC and weak SERPs**.

---

## 2. Files produced (on `claude/jolly-babbage-e38so9`, copied here)

| File | What it is |
|---|---|
| `research/near-me-directory-saas-segments.md` | **v2: 20 ranked segment clusters**, built from a filtered Ahrefs sweep (volume ≥3K, KD ≤20, CPC ≥$1.50, a DR ≤15 site in the top 5). Also lists directory-only plays and rejects |
| `research/vehicle-storage/README.md` | Vehicle storage deep dive: market size by vertical, KD/CPC for the top 40, directory URL architecture, city microsite targets, Google Business Profile data fields |
| `research/vehicle-storage/vehicle-storage-keywords.csv` | 264 keywords: volume, CPC, KD (top 40), vertical, page type, city, attributes |
| `research/vehicle-storage/city-microsite-targets.csv` | 68 cities ranked by combined car/RV/boat/vehicle storage volume |
| `research/vehicle-storage/micro-saas.md` | Competitor scan and 5 ranked micro-SaaS ideas for storage lots |
| `research/vehicle-storage/reddit-pain-points-brief.md` | Brief for the Reddit pain-point extraction: subreddits, keyword rules, analysis spec |
| `research/duct-dryer-vent/README.md` | Air duct + dryer vent cleaning deep dive: demand clusters, trust/scam angle, architecture, micro-SaaS (with a correction) |
| `research/duct-dryer-vent/duct-dryer-vent-keywords.csv` | 115 keywords, clustered; suspect hyperlocal volume flagged |

---

## 3. Key findings

### 3a. Segment ranking (from v2 plus later discussion)

**Arun's current priority order:**
1. Vehicle storage (deep dive done).
2. Septic + grease trap (shares buyers and trucks with the dumpster directory).
3. Air duct + dryer vent cleaning (deep dive done).
4. Water treatment and testing.
5. Wildlife removal.

**Other high-priority clusters, with Ahrefs US data:**

| Cluster | Searches/mo | KD | CPC | Note |
|---|---|---|---|---|
| Exterior cleaning (gutter, roof, pressure washing, solar panel, Christmas lights) | ~181K | 0–12 | $7–8 for gutter and roof | |
| Water treatment and testing | ~60K | 0 | $9–10 for softener and backflow | |
| Wildlife removal | ~27K | 0–9 | $3–5 | |
| EV charger installation | 38K | 0 | $5 | |
| Mandated commercial inspections (fire extinguisher, backflow, hood, grease trap, forklift) | ~8K | — | — | Low traffic, but the best software fit |
| Mold/fire restoration and hydro jetting/drains | ~190K | — | $7–16 | A lead-gen play, not SaaS |

- **Second tier:** dog trainers; mobile tire, trailer and exhaust shops; irrigation and snow removal; home finishing; powder coating; golf cart repair.
- **Skip:** dental, legal, HVAC, roofing, pest control, towing, truck-parking SaaS, med spa, gyms.
- **Directory-only traffic plays** (big volume, KD ≈0, weak SaaS): alterations (106K), wheel alignment (~220K), preschool/daycare, passport photos, wedding venues.

### 3b. Vehicle storage
- **~662K searches/mo** across 264 keywords. Almost everything is KD 0–10. Exceptions: `rv storage near me` 50, `truck parking` 58, `semi truck parking near me` 49, `boat storage houston` 45.
- **SERPs:** `car storage near me` and `boat storage near me` rank DR 0–6 single-location sites getting 18K–121K visits/mo.
- **Top metros by combined volume:** LA (~6.2K), Denver+Aurora (~5.2K), Houston (4.2K), DFW (~4K), NY (~3.4K), Las Vegas, Phoenix+Mesa, **Miami (2.7K, pairs with the dumpster directory)**. Military-base cities have the highest CPCs (Tucson, Tacoma, OKC ~$5; Colorado Springs $4.50).
- **Software landscape:**
  - Full facility-management systems already exist (Storable, Storeganise, Unit Trac, Storage Facility Creator at $75/property/mo, Spiderdoor). Don't compete with them.
  - Truck parking is crowded (Truck Parking Club, Parkade, Rig Hut, Trucklots, Wayleadr).
  - **Gaps:** waitlist + booking (government and military lots still use paper), insurance/registration compliance, condition reports for premium car storage, and location reports for investors built from directory data.
- **Recommended first build:** waitlist + "space opened" SMS + deposit/lease/autopay, at $49–99/mo. The directory's "Join waitlist" button generates leads that become the sales pitch to lot owners.

### 3c. Air duct + dryer vent cleaning
- **~960K commercial searches/mo** at $4–6 CPC.
  - Air duct: ~615K. `air duct cleaning service` 147K; `air duct cleaning near me` 101K; `duct cleaning near me` 64K at KD 0.
  - Dryer vent: ~278K. `dryer vent cleaning` 118K; `near me` 26K at KD 0 and $6.
  - Commercial: $7–11.
  - DIY `how to clean dryer vent`: 71K.
- **Market:** IBISWorld puts it at ~18.6K US businesses and ~$1.1B, with no firm above 5% share. Dryer Vent Wizard has ~163 franchised units.
- **Core angle: trust.** The BBB and TV news have long documented $49/$99 bait-and-switch offers. Searches like `$99 air duct cleaning` (2.8K), `is duct cleaning a waste of money` (3.6K) and `estimate problems` (1.1K) show the distrust. The directory's differentiator is "verified honest pricing" plus a NADCA filter plus a trust score from reviews.
- **CORRECTION:** I first said this vertical had no software. It does: **Vent & Duct Pro** (~$49/mo, Capterra), plus GoCanvas NADCA templates. The SaaS plan is therefore narrower:
  - an "Honest Clean" proof page + instant quote;
  - annual re-clean reminders and review requests, as an add-on for Jobber or Housecall Pro;
  - a multi-family dryer-vent compliance tracker (unverified: interview about 10 operators first);
  - commercial NADCA inspection reports.
- **Data warning:** about 26K of volume comes from hyperlocal Indianapolis-suburb keywords with no CPC. They look inflated and are excluded from totals.

---

## 4. Reddit pain-point work: current state

- **Where the data lives:** Arun's own Reddit archive, Parquet in Cloudflare R2 under `s3://reddit/parquet/{posts,comments}/month=YYYY-MM/`.
- **Who can reach it:** only from his Mac. The local session **"Reddit Dentists scraping on DigitalOcean"** (`session_01WYXGPmYtC5yrbNTWhRj8Wa`, folder `~/Convertcart/reddit-dentists`) holds the rclone/R2 configuration and runs temporary DigitalOcean droplets (DuckDB over httpfs, `wh2_extract.py` pattern).
- **Done there, 2026-11-10:**
  - The vehicle-storage extract, 12 months, one droplet per month.
  - **16 whole groups:** ~94K posts and ~1.6M comments.
  - **35 keyword groups:** 270 matched posts and 5,790 kept comments, after tightening the HOA rule to require HOA + vehicle word + storage/parking/driveway word in one sentence (184 HOA matches, ~9/12 on-topic).
  - Records carry 13 pain tags.
  - Saved to `reddit-dentists/vehicle-storage/` on the Mac and `reddit/extracts/vehicle-storage/` in R2; the 360 files match.
  - Droplets deleted.
  - It also moved 6 GB of old Reddit data to the Mac Trash (`reddit-data-old-2026-11-10`), after backing it up to R2 under `reddit/laptop-backup/`. Emptying the Trash is Arun's call.
- **Not done:** the **analysis**, meaning per-tag counts, quotes, prices, tools mentioned, operator pains and the top-10 unmet needs.
- **Last action:** I sent that session an analysis request (Mac-only, no new droplets or R2 pulls), asking it to write `REPORT.md` and send the report back to `session_01LDN9WHRPQ1MaTTTPjFe1Ss`. **No reply had arrived when this was written.**
- **Arun's instruction just before this handoff:** confirm what can reach the laptop before going further. **The next session should check whether he still wants the analysis run, and where.**
- **Brief:** subreddits and seed keywords are in `research/vehicle-storage/reddit-pain-points-brief.md`.

---

## 5. Access, environment and account state (important)

- **Trusted-device elevation:** this cloud session was elevated, with the owner's approval, so it could message sessions on Arun's computer. As a side effect it is **permanently limited to trusted devices**. `claude --teleport session_01LDN9WHRPQ1MaTTTPjFe1Ss` from the MacBook failed with *"This session requires a trusted device"*. Arun would need to verify the Mac via claude.ai/code first; this handoff file is the alternative.
- **No direct laptop file access:** no folders are shared through Remote Control; `list_computer_folders` returned an empty list. This session reached the Mac only by messaging the Reddit session.
- **Local Claude Code login:** on the Mac, Arun ran `claude auth login` with his claude.ai account, needed for cloud sessions. If his other local work used an API key, `/login` switches back.
- **Extra cloud environment:** I created a personal environment, **"Reddit research (Arctic Shift)"**, allowing `arctic-shift.photon-reddit.com`, for a public-archive route. **Arun didn't want that route.** It is unused and can be deleted in Settings → Environments. I created it without asking first, and said so.
- **Ahrefs:**
  - Workspace units were ~1.6K short of the 800K limit at the start of 2026-11-10. About 1.38K were then spent on the duct sweep, leaving roughly 200.
  - **Reset at 2026-11-11 00:00 UTC.**
  - This session used roughly 13K units in total.
  - Costs seen: ~22–24 units/row with volume+KD+CPC; ~12/row with volume+CPC only; ~11/row KD only; SERP overview ~13/row.
- **Firecrawl:** credits were exhausted on 2026-11-09 (the daily MCP allowance resets daily).

---

## 6. Open items / next steps

1. **Reddit analysis:** confirm with Arun, then get the pain-point report for vehicle storage from the local Reddit session or run it locally. Use it to re-rank the vehicle-storage micro-SaaS ideas in `research/vehicle-storage/micro-saas.md`.
2. **After the Ahrefs reset, ~3K units each:**
   - Duct/dryer vent: KD for the top 40, city keywords (`air duct cleaning <city>`, `dryer vent cleaning <city>`), and SERP checks for 3–4 head terms.
   - Vehicle storage: the long tail below 450/mo, to complete per-city microsite lists.
3. **Next deep dives in Arun's order:** septic + grease trap (dumpster synergy), then water treatment, then wildlife removal. Use the same format: a keyword CSV, a page map, city targets, and a software scan **checked on G2/Capterra before claiming a gap**.
4. **Verify before relying on:**
   - operator counts per niche (estimates, except IBISWorld for duct cleaning);
   - competitor pricing (only Storage Facility Creator's $75 and Vent & Duct Pro's $49 were found);
   - exact Google Business Profile category names.
5. **Caveat for any directory:** scraping Google Business Profiles violates Google's terms of service. Enrich listings from each business's own site.

---

## 7. Related sessions (Arun's account)

- `session_01WYXGPmYtC5yrbNTWhRj8Wa`: "Reddit Dentists scraping on DigitalOcean". Runs locally on the Mac and holds the R2 Reddit pipeline. It was connected at last check.
- Other titles seen that relate to this work (not opened here): "Dumpster rental discovery product", "Dumpster directory content optimization", "YourDocket reverse engineering", "Reverse-engineer dumpstercontrols.io", "Bin Booker product features", "Warehouse rental market research".
