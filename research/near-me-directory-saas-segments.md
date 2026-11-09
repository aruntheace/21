# "Near Me" Directory + Vertical SaaS: Segment Research (v2)

*Data: Ahrefs API v3, US database, pulled 2026-11-09. About 9,700 API units used in total.*

## How v2 was done

In v1 I picked about 120 keywords by hand. That missed many of the best segments.

For v2 I asked Ahrefs for **every** "... near me" keyword that met all of these at once:

- **Volume:** at least 3,000 searches a month.
- **Keyword difficulty (KD):** 20 or lower.
- **Cost per click (CPC):** at least $1.50, which shows businesses pay for these leads.
- **Weak results:** at least one site with domain rating 15 or lower already ranks in the top 5.

That returned the top 200 by volume. I then checked 55 more keywords by hand for rental, B2B, pet and specialty trades, because my v2 filter had accidentally excluded anything with "rent" in it.

Finally I grouped the keywords into **clusters**. One directory site and one software product cover every keyword in a cluster, so volumes below are cluster totals.

Still excluded: mainstream dental, medical, legal, insurance, car dealers, HVAC, roofing and pest control. They pass the KD filter, but the software side is crowded and the leads are already sold by big platforms.

---

## Top 20 clusters, ranked

Ranking weighs volume, CPC, how weak the current results are, and how thin the software market is. All numbers are US "near me" figures from Ahrefs. The "Software gap" column is my own read of the market.

| # | Cluster | Keywords inside (searches/mo · KD · CPC) | Cluster volume | Software gap |
|---|---|---|---|---|
| 1 | **Vehicle, boat and RV storage** | car storage 61K·0·$2 · boat storage 36K·2·$1.6 · RV storage 29K·50 · vehicle storage 27K·0·$2 · camper storage 11K·8 · trailer storage 9.1K·2 | **~173K** | **High.** Self-storage software is built for indoor units, not outdoor lots. Top results include **DR 0–6 storage sites getting 18K–121K visits a month** |
| 2 | **Air duct, dryer vent and chimney** | duct cleaning 58K·0·**$5** · dryer vent cleaning 26K·0·**$6** · chimney sweep 14K·28·$3.5 · hood cleaning 1K·0 | **~99K** | **High.** No vertical software. Needs inspection reports with before/after photos and annual reminders |
| 3 | **Exterior cleaning and seasonal** | gutter cleaning 55K·5·**$8** · gutter repair 26K·2·**$8** · pressure washing 25K·22 · power washing 20K·2·$4 · Christmas light installation 20K·0·$3 · window cleaning 13K·10 · roof cleaning 12K·12·**$7** · solar panel cleaning 10K·0·$3 | **~181K** | **Med-high.** Mostly generic field-service apps. Few instant-quote tools that work from satellite measurement |
| 4 | **Septic** | septic pumping 51K·50 · septic repair 36K·**2**·$3.5 · septic tank repair 34K·**1**·$3.5 · septic service 14K·2 · grease trap 0.9K·0·$6 | **~136K** | **Medium.** ServiceCore plus small tools. Top results include DR 1–11 local sites |
| 5 | **Water treatment and testing** | water testing 31K·0·$3 · water softener companies 17K·0·**$9** · well drilling 5.9K·47 · well pump repair 4.9K·43·$6 · backflow testing 1.6K·0·**$10** | **~60K** | **High.** Fits a dealer CRM with salt-delivery routes, filter-change reminders and backflow compliance filing |
| 6 | **Wildlife removal** | bat removal 10K·2·$3 · wildlife removal 7.1K·1·**$4.5** · squirrel removal 4.7K·6·**$5** · raccoon removal 3.6K·9·$3.5 · snake removal 1.9K·0·$3 | **~27K** | **High.** Almost no vertical software. Needs trap-check logs (required by state law), exclusion quotes and warranty tracking |
| 7 | **Drain and specialty plumbing** | hydro jetting 46K·0·**$10** · drain cleaning companies 14K·1 · garbage disposal repair 11K·0·**$16** · leak detection 9.5K·1·$6 · sewer camera 3.3K·0·$10 | **~84K** | **Low for software** (plumbers already use ServiceTitan and Housecall Pro). **Very strong for selling leads**: results are Roto-Rooter, Yelp and DR 1–2 local sites |
| 8 | **Mold, fire and water restoration** | mold remediation 61K·0·**$7** · water damage restoration services 20K·5 · mold removal company 16K·2·$6 · fire restoration 8.6K·0·**$9** | **~106K** | **Medium** (Encircle, DASH). The money here is selling leads |
| 9 | **Dog training, boarding and walking** | dog boarding 115K·8·$2 · dog training 67K·3·$1.8 · dog daycare 21K·38 · dog trainers 15K·6 · dog hotels 13K·0 · cat boarding 12K·12 · mobile vet 11K·0 · dog walker 3.9K·0·$2.5 | **~258K** | Boarding software is crowded (Gingr, MoeGo). **Dog-trainer software is thin**: packages, homework videos, progress tracking |
| 10 | **EV charger and home window tinting** | EV charger installation 38K·0·**$5** · house window tinting 19K·2·$2.5 · home window tinting 11K·0·$3 | **~68K** | **High.** Needs a quoting tool (EV: panel-load check and rebates; tint: film quotes from window measurements) |
| 11 | **Specialty auto (independent shops)** | exhaust shop 22K·0 · diesel mechanic 16K·0·$2.5 · car window repair 11K·6 · trailer repair 9.6K·0 · mobile tire service 6.4K·0 · trailer hitch installation 6.6K·1 | **~72K** | **Med-high** for mobile tire, trailer and exhaust shops (Fullbay only covers heavy-duty). General auto shops are crowded |
| 12 | **Detailing and paint protection** | car detailing 136K·5·$1.5 · ceramic coating 28K·0·$2.5 · detailing 25K·0 · mobile detailing 19K·60 · paint protection film (PPF) 14K·13·**$4** | **~222K** | **Medium** (Urable, Mobile Tech RX). Huge directory traffic |
| 13 | **Irrigation, turf and snow** | sprinkler repair 15K·61 · irrigation repair 14K·**0**·$3.5 · snow removal 12K·0 · artificial turf 4.5K·0 | **~45K** | **Med-high.** Needs zone maps, seasonal start-up and shut-down routes, and snow logs that protect against slip-and-fall claims |
| 14 | **Independent equipment and dumpster rental** | dumpster rental 60K·36 · skid steer rental 9.8K·2 · scissor lift rental 8K·4 · mini excavator rental 2.8K·41 · roll off dumpster 2.1K·0·$2.5 · storage container rental 1.4K·0·**$6** | **~84K** | **Medium.** Independent yards are underserved. Your **Miami dumpster directory belongs here** ("dumpster rental miami": 1K/mo, KD 0, $8 CPC) |
| 15 | **Home finishing specialty** | deck staining 11K·1·$3.5 · epoxy flooring 10K·31 · concrete repair 8.4K·0·$4.5 · cabinet painting 8.3K·0·**$6** · tile & grout cleaning 4K·0·$3.5 | **~42K** | **High.** Needs before/after photo quoting and sq-ft estimators |
| 16 | **Medical weight-loss clinics (GLP-1)** | B12 shots 16K·0 · Ozempic near me 11K·10·**$12** · tirzepatide near me 9.8K·1·**$10** | **~37K** | **Medium.** Selling leads is very valuable, but medical advertising rules apply |
| 17 | **Laser tattoo removal and aesthetics** | microneedling 34K·0 · lip filler(s) 52K·0 · Hydrafacial 27K·0 · tattoo removal 24K·0·$3 · chemical peel 12K·0 | **~150K** | Med-spa software is crowded. Tattoo-removal studios specifically are thin |
| 18 | **Mandated commercial inspections (B2B)** | forklift repair 2.3K·0·$3.5 · fire extinguisher inspection 1.9K·1·$2.5 · backflow 1.6K·$10 · hood cleaning 1K · grease trap 0.9K·$6 | ~8K | **Best software fit, smallest traffic.** Due-date compliance software sells itself |
| 19 | **Towing** | tow truck 132K·**1**·$3 · towing company 34K·11 | **~166K** | Towbook is the leader. Strong urgent-call lead selling |
| 20 | **Round-1 picks that still hold** | powder coating 21K·0 · golf cart repair 9.4K·0 · mobile RV repair 11K·0 · land surveyor 7.6K·5 · piano tuner 5.6K·13 | ~55K | See v1 notes. Low CPC but very thin software |

### Directory-only traffic plays (KD ≈ 0, big volume, weak software opportunity)

These earn from ads and leads, not software.

| Keyword | Volume | KD |
|---|---|---|
| alterations | 106,000 | 0 |
| wheel alignment / alignment | ~220,000 | 0 |
| preschool / daycare | ~138,000 | 1–9 |
| wedding venues | 51,000 | 0 |
| passport photos | 45,000 | 0 |
| print shop | 42,000 | 12 |
| laundry service / wash and fold | 32,000 | 0–1 |
| jet ski rental | 19,000 | 0 |
| tutoring ($5 CPC) | 18,000 | 0 |
| engraving | 18,000 | 3 |
| barber school | 15,000 | 0 |
| CNA programs | ~24,000 | 0 |

---

## What the results pages showed (organic results under the map pack)

| Keyword | Who ranks |
|---|---|
| car storage near me | `selfstorageks.com` **DR 0** (121K traffic), `ustorwichita.com` **DR 6**, Public Storage DR 73, Yelp, Facebook group |
| boat storage near me | **DR 0–6** storage sites at #3, #6, #8 and #10, Neighbor.com DR 73, Yelp |
| hydro jetting near me | Roto-Rooter ×2, Yelp, **DR 1–2** local plumbers, Reddit, YouTube |
| septic tank pumping near me | Yelp, **DR 1, 11 and 4** local septic companies at #4–6 |
| grease trap cleaning near me | Yelp ×7, **DR 0–1** sites |
| chimney sweep near me | Yelp, Reddit, Angi, BBB, **DR 0** sweeps |
| powder coating near me | Yelp, Facebook, **DR 1–3** shops, powdercoatingnearme.com (DR 9) |
| golf cart repair near me | thecartfinder (DR 36), golfcartresource (DR 64), Yelp |
| mobile RV repair near me | rvhelp.com (DR 70), Yelp, Road Rescue (DR 45) |
| dumpster rental miami | franchise sites (DR 38–56), Yelp, a **DR 8** local hauler |

**Pattern:** in most of these clusters, nobody structured owns the results. Yelp's generic search pages and DR 0–10 single-location sites hold the slots, so a real directory with city pages can take them.

---

## Recommended build order

1. **Vehicle, boat and RV storage.** It has the biggest volume with the lowest KD, and the results are full of DR 0 sites. The software is outdoor-lot management: lot map, waitlist, recurring billing, gate codes and insurance documents. Lot owners pay $100–300/mo.
2. **Air duct and dryer vent cleaning.** About 84K searches, all at KD 0 with $5–6 CPCs, and no vertical software. Build inspection reports, annual reminders and a review-request flow.
3. **Waste and septic (dumpster + septic + porta potty + grease trap).** This continues what you've already started in Miami. Build one dispatch and asset-tracking tool and run four directories off it.
4. **Water treatment and testing.** High CPCs and an obvious recurring workflow (salt delivery, filter changes, backflow certificates).
5. **Wildlife removal.** Small but rich. Operators pay well and no one builds for them.

## Caveats

- **"Near me" volumes are national.** Ahrefs checked most of these results from Wichita, KS. Real traffic comes from `<service> <city>` pages, usually 50–1,500 searches a month each.
- **KD 0** means the top pages have few backlinks. It does not mean no competition; the map pack still sits above them.
- **Operator counts and software competitor names are my estimates, not Ahrefs data.** Check each one on G2 or Capterra before you build.
- **Google Business Profile data:** scraping it violates Google's terms. Plan to enrich listings from each business's own website, which is also what makes a directory rank.
- **Ahrefs budget:** about 5K units remain until the 2026-11-11 reset.
