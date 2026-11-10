# Air Duct + Dryer Vent Cleaning: Deep Dive (Directory + Micro-SaaS)

*Data: Ahrefs API v3 (US), pulled 2026-11-10, plus web research. Keyword file: [`duct-dryer-vent-keywords.csv`](duct-dryer-vent-keywords.csv), 115 keywords.*

**Coverage limits.** The Ahrefs units left before the 11 Nov reset allowed one sweep, so the list stops at about 1,100 searches/mo. Difficulty is only known for the near-me terms from earlier research.

**Still to pull after the reset (about 3K units):**
- Difficulty for the top 40 keywords.
- City keywords (`air duct cleaning <city>`, `dryer vent cleaning <city>`).
- Results-page checks for 3–4 head terms.

---

## 1. Demand

| Cluster | Searches/mo | CPC range | Main keywords |
|---|---|---|---|
| **Air duct cleaning** | **~615K** | $1–$9 (mostly $4–6) | air duct cleaning service **147K** · air duct cleaning near me **101K** · air duct cleaning 72K · duct cleaning near me 64K (**KD 0**) · duct cleaning 62K ($6) · air duct cleaning services 51K |
| **Dryer vent cleaning** | **~278K** | $3.50–$6 | dryer vent cleaning **118K** ($4.50) · dryer vent cleaning near me 26K (**KD 0**, $6) · dryer vent cleaning service 14K ($6) · clothes dryer vent cleaning 14K · dryer air duct cleaning 13K |
| **Dryer vent repair** | ~45K with good CPC | $5–6 | dryer vent repair near me 12K · dryer vent repair 10K · dryer vent installation near me 8.5K ($4.50) |
| Dryer vent install / replace (mostly DIY) | ~49K | $0.30–0.50 | dryer vent installation 10K · dryer vent replacement 11K · line installation 9.9K |
| **Commercial duct cleaning** | ~21K | **$7–11** | commercial duct cleaning 12K ($7) · commercial … near me 4.4K · commercial air duct cleaning services 1.7K (**$11**) |
| DIY how-to guides | ~87K | <$0.10 | how to clean dryer vent **71K** · from outside 1.7K · how often to clean dryer vent 1.1K |
| Pricing guides | ~15K | $2–4 | air duct cleaning cost 5.6K · **$99 air duct cleaning 2.8K** · duct cleaning cost 2.6K · dryer vent cleaning cost 2.6K |
| **Trust / skepticism** | ~4.7K | $1.60 | **is duct cleaning a waste of money 3.6K** · air duct cleaning estimate problems 1.1K |
| Products (affiliate) | ~67K | <$0.30 | dryer vent 35K · magnetic dryer vent 16K · tools, caps, periscope vents |
| Competitor brands | 5.5K | — | Dryer Vent Wizard 3.6K · Fresh Air 1.9K |

**Total commercial demand (duct + dryer + repair + commercial): about 960K searches/mo, at $4–6 a click.** For comparison, all of vehicle storage was about 660K at $1.50–2.

> **Data warning.** About 26K of volume comes from hyperlocal keywords with no CPC, such as "residential air duct cleaning old bargersville / westfield / smith valley / sheridan / noblesville / stilesville". Most are Indianapolis suburbs. A tiny suburb at 1–2K/mo with no advertisers usually means automated or manipulated searches, not real demand. They're flagged in the CSV, and I left them out of the totals and city plans.

## 2. Competition

- **Earlier SERP data:** `duct cleaning near me` and `dryer vent cleaning near me` are both **KD 0**, with DR 0–10 local sites in the top 5. That came from the round-2 filtered sweep; the head terms haven't been checked yet.
- **The industry is highly fragmented.** IBISWorld counts **~18,600 air duct cleaning businesses in the US**, a **~$1.1B** market where **no company has more than 5% share**.
- **Franchises are small.** Dryer Vent Wizard has **~163 franchised units**, averaging about **$237K** gross revenue per unit with a 10% royalty. Other brands include Ductz and Stanley Steemer's duct service. Most of the 18.6K businesses are independents: your directory listings and software customers.
- **Trust is broken.** The BBB and TV news have warned about **$49/$99 "whole-house" bait-and-switch** offers that end in $1,000–1,800+ bills, for over a decade. Searches like "$99 air duct cleaning" (2.8K), "is duct cleaning a waste of money" (3.6K) and "estimate problems" (1.1K) show consumers are wary. Credible benchmark: a real whole-system clean typically costs **$450–1,000** for an average home.

**What this means for the directory:** "Verified honest pricing" is the angle. Show upfront per-system pricing, NADCA certification and real reviews, with no $99 bait. Yelp, Angi and the lead-gen networks can't credibly offer this, because the bait-and-switch operators advertise with them.

## 3. Directory site architecture

```
/air-duct-cleaning/                -> air duct cleaning (service, near me, services, company, companies, best) ~615K
/dryer-vent-cleaning/              -> dryer vent cleaning (+ near me, service, professional, clothes/laundry dryer) ~278K
/dryer-vent-repair/                -> repair + installation "near me" (high-CPC subset) ~30K
/commercial-duct-cleaning/         -> commercial, hvac and ac duct cleaning; $7-11 CPC ~30K
/{service}/{state}/{city}/         -> city pages (city keyword pull pending)
/listing/{company}/
Filters: NADCA certified · CSIA-certified dryer exhaust tech · upfront price listed · residential / commercial ·
         also does chimney (the "air duct cleaning and chimney cleaning" query, $8 CPC)

/guides/
  air-duct-cleaning-cost/            -> cost (5.6K) + how much (1.5K) + services cost (1.3K) + duct cleaning cost (2.6K)
  dryer-vent-cleaning-cost/          -> 2.6K
  99-dollar-duct-cleaning-scam/      -> $99 air duct cleaning (2.8K) + estimate problems (1.1K)
  is-duct-cleaning-worth-it/         -> is duct cleaning a waste of money (3.6K)
  how-to-clean-dryer-vent/           -> 71K + variants ~80K. Traffic magnet; affiliate links to tools and magnetic vents
  how-often-clean-dryer-vent/        -> 1.1K. Fire-risk data and the annual reminder hook
```

**Why the dryer vent guides matter.** NFPA counts about **13,800 home fires a year** where the dryer was the ignition source. About **32%** were caused by failure to clean, with lint as the leading fuel. That's the credible safety reason for an annual clean, and it drives the reminder software below.

## 4. Data to collect per company

**From Google Business Profiles.** Pull the "Air duct cleaning service" category plus HVAC and chimney companies that mention dryer vents; confirm the exact category names. Fields: name, phone, website, address or service area, hours, rating, reviews.

**From each company's site and its reviews:**
- NADCA membership (verify against NADCA's member directory).
- Upfront pricing: per vent, per system, per dryer vent.
- Residential and/or commercial.
- Whether it does dryer vent repair or rerouting, and roof vents.
- Chimney and fireplace services.
- Before/after photos or video provided.
- Review mentions of "upsell", "bait", "$99" or "scam". These become a **trust score**, the directory's unique feature.

## 5. Micro-SaaS opportunities

**Correction to my earlier ranking:** I said this vertical had no software. It does. **Vent & Duct Pro** is a duct and vent cleaning field-service app (scheduling, routing, branded safety reports, re-clean dates), starting at about **$49/mo flat** on Capterra. **GoCanvas** has a NADCA condition-report form template. Generic field-service apps (Jobber, Housecall Pro) are common. So don't build another all-in-one; build narrower tools.

| # | Idea | Problem it solves | Price | Gap |
|---|---|---|---|---|
| 1 | **"Honest Clean" proof page + instant quote** | Consumers don't trust duct cleaners. Operators who don't do bait-and-switch can't prove it | $39–79/mo | **High.** Ties to the directory trust score. Nobody sells trust as a product |
| 2 | **Multi-family dryer vent compliance tracker** | Apartment complexes, condos and HOAs need building-by-unit vent cleaning schedules and certificates for insurers and fire marshals | $99–299/mo | **High (verify).** B2B, recurring, documentation-heavy. Sell to cleaners who serve properties, or to property managers |
| 3 | **Annual re-clean reminder + review engine** (add-on for Jobber / Housecall Pro) | Dryer vent and duct cleaning recur every 1–3 years, and most operators never re-contact past customers | $29–49/mo | Medium. Vent & Duct Pro sets re-clean dates, but only inside its own app |
| 4 | **Commercial duct inspection reports** (NADCA ACR-aligned) | Commercial jobs ($7–11 CPC) need formal reports: supply, return, exhaust, coils, dampers | $79–149/mo | Medium. GoCanvas templates exist but are generic |

**Recommended wedge: #1 + #3 as one product** ("trust + rebooking"), with #2 as the B2B upsell.

Path to $5–10K MRR:
- 100–150 operators at ~$59, from a pool of ~18.6K businesses.
- Or 30–50 property-management or large-cleaner accounts on #2.

## 6. Build order

1. **Directory first.** Hubs for air duct, dryer vent, dryer vent repair and commercial, plus the trust filters (NADCA, upfront price, no-bait reviews). City pages once the city keywords are pulled.
2. Publish the **cost guide**, the **$99-scam guide** and **how to clean a dryer vent**. These are the traffic and trust anchors.
3. **"Claim your listing → get a free Honest Clean profile."** Free tier of #1, upsell to quotes plus reminders.
4. Interview 10 operators about #2 before building it. It is the highest-value idea but the least verified.

## Sources

**Market and software**
- [IBISWorld: Air Duct Cleaning Services, number of businesses](https://www.ibisworld.com/united-states/number-of-businesses/air-duct-cleaning-services/6218) and [market size](https://www.ibisworld.com/united-states/market-size/air-duct-cleaning-services/6218/)
- [Dryer Vent Wizard franchise data (Franzy)](https://franzy.com/franchises/dryer-vent-wizard) and [Zee Report](https://zeereport.com/reports/dryer-vent-wizard)
- [Vent & Duct Pro on Capterra](https://www.capterra.com/p/10044876/Vent-Duct-Pro/)
- [GoCanvas NADCA Air Ducts Condition Report](https://gocanvas.com/mobile-forms-apps/12042-Air-Ducts-Condition-Report-NADCA)
- [NADCA commercial checklist](https://nadca.com/commercial-checklist)

**Bait-and-switch warnings**
- [BBB bait-and-switch duct cleaning warning (PDF)](https://www.sheriff-okaloosa.org/wp-content/pdfs/ssdrop/Feb_-1-BBB-Beware-bait-switch-air-duct-cleaning.pdf)
- [BBB St. Louis pricing scam warning (Patch)](https://patch.com/missouri/townandcountry-manchester/bbb-warns-against-u-s-air-ducts-pricing-scam)
- [FOX 5 DC duct cleaning scam report](https://www.fox5dc.com/news/more-homeowners-say-air-duct-cleaning-crew-scammed-them-following-fox-5-report)

**Dryer fire data**
- [USFA dryer fire data (Claims Journal)](https://www.claimsjournal.com/news/national/2012/08/14/211886.htm)
- [Fire Engineering: differing dryer-fire counts (USFA vs NFPA)](https://www.fireengineering.com/?p=291616)
