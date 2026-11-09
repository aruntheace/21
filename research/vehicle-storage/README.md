# Vehicle Storage: Keyword Deep Dive (Directory + City Microsites)

*Data: Ahrefs API v3, US, pulled 2026-11-09.*

## Files

| File | What's in it |
|---|---|
| [`vehicle-storage-keywords.csv`](vehicle-storage-keywords.csv) | **264 keywords**. Columns: volume, CPC (USD), keyword difficulty (KD, 0–100, filled for the top 40), vertical, page type, city, attributes |
| [`city-microsite-targets.csv`](city-microsite-targets.csv) | **68 cities** ranked by combined search volume across car, RV, boat and vehicle storage |

**Coverage limit:** Ahrefs returned the top 250 matching keywords by volume, so the floor is about **450 searches/mo**. Smaller cities and long-tail combinations (e.g. "covered rv storage peoria") exist below that. After the 2026-11-11 unit reset, a sweep of `rv storage` / `boat storage` / `car storage` from 50–450 volume will fill out the long tail for each city.

---

## 1. Market size

| Vertical | Keywords | Searches/mo | Notes |
|---|---|---|---|
| Car / auto / classic car storage | 97 | **218,000** | Biggest vertical. Many urban city keywords |
| RV / camper / travel trailer storage | 63 | **144,000** | Strongest in the Sun Belt (FL, AZ, TX, NV). Highest **lot-owner willingness to pay** |
| "Vehicle storage" (generic) | 22 | **107,500** | Head term, 56K at KD 4 |
| Boat storage | 33 | **107,000** | Coastal and lake cities. Seasonal |
| Truck / semi parking | 21 | **48,600** | Different buyer (truckers). Truck Parking Club owns the brand term (19K) |
| Trailer storage | 5 | 15,300 | |
| Motorcycle storage | 5 | 13,900 | Low CPC, much of it product searches |
| RV + boat combined | 7 | 8,100 | |
| **Total** | **264** | **~662,000** | |

### Difficulty and CPC on the main keywords

| Keyword | Vol | KD | CPC |
|---|---|---|---|
| car storage near me | 61,000 | **0** | $2.00 |
| vehicle storage | 56,000 | **4** | $2.00 |
| car storage | 41,000 | **0** | $1.80 |
| boat storage / boat storage near me | 36,000 / 36,000 | **0 / 2** | $1.50 / $1.60 |
| rv storage | 36,000 | **1** | $1.80 |
| rv storage near me | 29,000 | 50 | $1.60 |
| vehicle storage near me | 27,000 | **0** | $2.00 |
| truck parking near me | 11,000 | **0** | $0.90 |
| camper storage near me | 11,000 | 8 | $1.70 |
| car storage units near me | 10,000 | **0** | $2.00 |
| motorcycle storage | 9,700 | **0** | $0.70 |
| trailer storage near me | 9,100 | 2 | $1.90 |
| indoor rv storage near me | 7,200 | 2 | $1.30 |
| auto storage near me | 6,800 | **0** | $2.00 |
| vehicle storage facilities near me | 6,100 | 10 | $2.00 |
| indoor car storage | 5,600 | 1 | $1.60 |
| outdoor boat storage | 4,900 | **0** | $1.30 |
| cheap car storage | 2,100 | **0** | **$2.50** |
| car storage insurance | 900 | 3 | **$11.00** |
| truck parking (head) | 8,000 | 58 | $1.10 |
| classic car storage | 500 | 30 | $1.30 |

Almost every keyword sits at KD 0–10. The exceptions are `rv storage near me` (50), `truck parking` (58), `semi truck parking near me` (49) and `boat storage houston` (45).

Earlier result-page checks showed `car storage near me` and `boat storage near me` ranked by **DR 0–6 single-location storage sites** that get 18K–121K visits a month, plus Public Storage, Neighbor.com and Yelp. A structured directory can take those slots.

---

## 2. Directory site architecture (keywords mapped to pages)

```
/                                   -> "vehicle storage near me", "vehicle storage" (83K)
/car-storage/                       -> car storage (+ near me, units, unit, facility, rental, lot)  (~135K)
/rv-storage/                        -> rv storage (+ near me, facility, units) + camper / travel trailer (~95K)
/boat-storage/                      -> boat storage (+ near me, units, facility) + boat trailer (~90K)
/trailer-storage/                   -> trailer storage (+ near me, outdoor)          (~15K)
/motorcycle-storage/                -> motorcycle storage (+ near me, outdoor)      (~14K)
/truck-parking/                     -> truck / semi parking (+ monthly, overnight, daily) (~30K excl. brand)

  Filter pages (one per vertical), ~70K combined:
  /rv-storage/indoor/               -> indoor rv storage (+ near me) 11.5K, inside, enclosed
  /rv-storage/outdoor/              -> outdoor / outside rv storage 3.9K
  /rv-storage/climate-controlled/   -> 1.2K
  /rv-storage/cheap/                -> cheap / affordable rv storage 3.0K (cheap rv & boat: $7 CPC)
  /car-storage/indoor/              -> indoor / inside car storage 8.0K
  /car-storage/outdoor/             -> outdoor car storage 7.7K
  /car-storage/climate-controlled/  -> 1.3K ($3.50 CPC)
  /car-storage/long-term/           -> long term car/vehicle storage 3.1K
  /car-storage/cheap/               -> cheap car storage (+ near me) 3.5K ($2.50)
  /car-storage/classic/             -> classic car storage 1.0K
  /car-storage/winter/              -> winter car storage near me 600 (northern cities, seasonal)
  /boat-storage/indoor/ | /outdoor/ | /climate-controlled/ | /cheap/

  City pages: /{vertical}/{state}/{city}/   e.g. /rv-storage/fl/fort-myers/
  Listing pages: /listing/{facility-slug}/

/guides/
  car-storage-cost/       -> how much is car storage (+ per month, cost, prices) ~2.2K
  rv-storage-cost/        -> how much is rv storage (+ near me prices) ~1.9K
  boat-storage-cost/      -> boat storage cost / prices / per month ~1.6K
  car-storage-insurance/  -> car storage insurance ~1.1K. **$11 CPC: affiliate insurance leads**
  truck-parking-cost/     -> how much is truck parking (+ per month)
  start-rv-storage-business/, truck-parking-lot-business/, truck-parking-zoning/
      -> lot-owner content. These readers are your future software customers
```

### Competitor brand terms (don't target these; study the sites)

| Brand | Searches/mo |
|---|---|
| Truck Parking Club | 19,500 |
| RecNation RV & Boat Storage | 1,100 |
| Peak Auto Storage | 800 |
| CubeSmart car storage | 800 |
| Neighbor car storage | 700 |
| Spring Auto Storage | 600 |

- **Neighbor.com** is a peer-to-peer marketplace (DR 73). Your closest directory competitor.
- **Truck Parking Club** is a booking marketplace for truck parking. It proves truckers pay online.
- **RecNation** is a roll-up of RV and boat storage lots. It shows the lots are being consolidated, and that independents need software to compete.

---

## 3. City microsite targets

These are the top cities by combined volume across car, RV, boat and vehicle storage. Only keywords with 450+ searches/mo are counted, so true totals are higher.

| # | City | Combined vol | Split | Max CPC | Microsite angle |
|---|---|---|---|---|---|
| 1 | **Houston** | 4,200 | car 1.3K · rv 1.1K · boat 1.1K · vehicle 700 | $2.50 | All-vehicle site. Boat KD 45, the rest are easy |
| 2 | **Las Vegas** | 3,050 | rv 1.2K · car 700 · vehicle 700 · boat 450 | $2.50 | RV first (HOA bans on driveway RVs) |
| 3 | **Denver** (+ Aurora 2.4K) | 2,800 + 2,400 | car 2.3K · rv 1.4K · vehicle 500 | $3.00 | **Denver metro is 5.2K combined**. Car storage KD 0 |
| 4 | **Miami** | 2,700 | car 1.2K · rv 1.0K · boat 500 | $2.50 | **Pairs with your Miami dumpster directory.** Car storage KD 0 |
| 5 | **Colorado Springs** | 2,500 | car 1.3K · rv 700 · boat 500 | **$4.50** | Military base: deployment car storage |
| 6 | **Atlanta** | 2,500 | car 1.5K (KD 28) · vehicle 1.0K | $2.00 | |
| 7 | **Salt Lake City** | 2,400 | car 1.1K · boat 700 · rv 600 | $3.00 | Lake Powell boats |
| 8 | New York (+ NYC, Jersey City) | 3,400 | car 2.9K · rv 500 | $2.50 | Urban car storage. Expensive, so high lead value |
| 9 | Chicago | 2,400 | car 1.1K · rv 800 · vehicle 500 | $1.60 | Winter storage season |
| 10 | San Diego | 2,200 | car 1.4K · rv 800 | $2.00 | |
| 11 | Columbus | 2,050 | car 1.6K · rv 450 | $2.00 | |
| 12 | Fort Worth (+ Dallas 1.35K, Arlington 600) | 3,950 | rv 1.9K · car 2.0K | $2.50 | **DFW metro is ~4K** |
| 13 | Myrtle Beach | 2,000 | boat 700 · car 700 · rv 600 | $1.40 | Tourist / second-home market |
| 14 | Phoenix (+ Mesa 950) | 2,750 | car 1.3K · rv 1.45K | **$4.00** | Snowbird RV season |
| 15 | **Tucson** | 1,700 | rv 1.0K (KD 4) · car 700 | **$5.00** | Highest CPC of any city |
| 16 | **Fort Myers** (+ Naples, Cape Coral) | 2,100+ | rv 1.6K (KD 5) | $2.50 | Snowbirds |
| 17 | Los Angeles (+ Long Beach 1.7K, Riverside 1.4K, OC, Irvine) | 6,200 | car 5.2K · rv 1.0K | $2.00 | **LA metro is the biggest single market** |
| 18 | San Antonio | 1,800 | car 1.2K · rv 600 | $2.50 | Military |
| 19 | **Tacoma** / Spokane | 1,300 / 1,400 | car + rv | **$5.00** / $1.60 | JBLM base (Tacoma) |
| 20 | **Oklahoma City** | 1,300 | car 700 · rv 600 | **$5.00** | Tinker AFB |

The full list of 68 cities is in `city-microsite-targets.csv`.

**Microsite pattern:** `{city}vehiclestorage.com` or `{city}rvstorage.com`, as 5–15 pages:

- **Home** targets `{vertical} storage {city}` for every vertical.
- **One page per vertical** (car, rv, boat).
- **One page per filter** (indoor, covered, cheap).
- **A local price guide** ("how much is rv storage in Tucson").
- **One page per facility**, built from Google Business Profile data.

**Military towns** (Colorado Springs, Tacoma, OKC, San Antonio) show much higher CPCs, because deployment storage is urgent and long-term. That's a good angle for content.

---

## 4. Data to collect per facility (from Google Business Profiles plus each facility's website)

**From Google Business Profiles:** name, address, coordinates, phone, website, hours, gate hours, rating, review count, photos and category.

Categories to pull (confirm the exact names in the Google Business Profile category list):

- "RV storage facility"
- "Boat storage facility"
- "Self-storage facility", filtered by "vehicle" or "car" in the name or reviews
- "Truck parking" or "Parking lot for trucks"

**From the facility's own website or a phone call.** These fields drive the filter pages and the conversions:

- Indoor, covered or open.
- Climate controlled.
- Maximum space length (25/35/45/50 ft).
- 24/7 access and keypad gate.
- Security cameras.
- Dump station, power hookups, wash bay.
- Monthly price from $X.
- Waitlist (yes/no).
- Whether insurance is required.

**Use review text to enrich listings.** Mentions of "waitlist", "full", "gate code", "clean" and "secure" become listing tags.

## 5. Software for these operators

The directory itself becomes the list of potential customers. Facility owners claim their listing, and that's where you start selling.

1. **Waitlist + online reservations** ($49–99/mo). Many RV lots run full with phone waitlists.
2. **Outdoor lot manager** ($99–249/mo):
   - Space map by length.
   - Recurring billing.
   - Gate code provisioning.
   - Insurance and registration document collection with expiry alerts.
   - Late-fee and lien workflow.
3. **Truck parking**: daily, weekly and monthly booking for independent lot owners. Truck Parking Club proves demand; independents need their own booking page.

The `start rv storage business`, `truck parking lot business` and `zoning` searches show lot owners are actively searching. Write guides for them to bring in software leads.
