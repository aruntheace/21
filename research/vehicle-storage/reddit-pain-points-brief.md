# Brief: Reddit pain points for vehicle storage (run in the "Reddit Dentists scraping on DigitalOcean" session)

Reuse the warehouse-space pipeline: the wh2_extract.py pattern, temporary droplets, and DuckDB over s3://reddit/parquet. Only matching rows should come back. Use the full month range up to Sep 2026. If the estimated cost is over about $30, report the estimate before launching.

## Groups

**Whole groups** (all posts, plus comments on them):
RVLiving, GoRVing, rvs, fulltimerv, Rvmechanics, TravelTrailers, Campers, boating, Boats, sailing, pontoonboats, classiccars, projectcar, selfstorage, Truckers, HOA

**Keyword-only groups** (only posts and comments that match the rules below):
- Vehicles: cars, motorcycles, Corvette, Porsche, Miata, Jeep
- Military: military, army, AirForce, navy
- Business: realestateinvesting, smallbusiness, Entrepreneur
- Legal and money: legaladvice, personalfinance, homeowners
- Metros: houston, Dallas, LasVegas, vegas, phoenix, Miami, orlando, LosAngeles, chicago, denver, Tucson, SaltLakeCity, coloradosprings, sandiego, Austin, sanantonio, tampa, FortMyers, Jacksonville

## Keyword rules

Case-insensitive. Name each rule, so every record lists the rules it matched.

| Rule | Pattern |
|---|---|
| storage_type | `(rv\|boat\|car\|auto\|vehicle\|camper\|trailer\|motorcycle\|bike\|5th wheel\|fifth wheel\|travel trailer\|toy hauler\|classic car\|truck)\s+(storage\|parking)` |
| storage_lot | `storage (lot\|yard\|facility\|unit\|space\|spot)` near a vehicle word |
| where_store | `where (do\|should\|can) (you\|i\|we) (store\|park\|keep) ... (rv\|boat\|camper\|trailer\|car\|motorcycle\|bike\|truck)` |
| store_my | `(store\|storing\|stored\|park\|parking) (my\|our) (rv\|boat\|camper\|trailer\|car\|motorcycle\|truck\|semi)` |
| hoa_vehicle | `hoa` plus `(rv\|boat\|trailer\|camper\|truck)` in the same text |
| covered_indoor | `(covered\|indoor\|enclosed\|climate controlled) (storage\|parking)` |
| waitlist | `(waitlist\|waiting list\|wait list)` near `storage` |
| deployment | `deploy(ment\|ed\|ing)` plus `(store\|storage)` plus `(car\|vehicle\|truck\|motorcycle)` |
| truck_parking | `truck parking`, `park (my\|the) (semi\|rig\|truck)`, or `overnight parking` |
| winter_storage | `winter(ize\|izing)? .{0,30}(storage\|store)` |
| operator | `(rv\|boat\|vehicle) storage (business\|lot\|facility)` plus `(start\|own\|run\|build\|invest\|zoning\|tenant\|lien\|auction\|abandoned)` |

## Analysis

Sort matches into pain categories:

- **Customer side:**
  - availability and waitlists
  - price and price increases
  - distance and access hours
  - security and theft (catalytic converters, batteries, solar panels)
  - damage while stored (rodents, mold, hail, sun, flood, hurricanes)
  - HOA or city bans on driveway parking
  - insurance
  - battery and tire upkeep
  - no covered space for tall rigs
  - scams (Craigslist, Neighbor)
  - disputes with the owner, and liens
  - long-term storage during deployment
  - winter storage
- **Operator side:**
  - tenants who don't pay
  - abandoned vehicles
  - liens and auctions
  - handling the waitlist
  - gate access
  - insurance
  - zoning
  - pricing
  - complaints about software
  - theft and liability

Add new categories as they appear.

For each category, report:
- post and comment counts, plus the trend by year
- top subreddits and cities
- 5–8 verbatim quotes, each with its permalink and score
- tools or software that people mention or wish existed
- prices people say they pay

## Output

Save the matched records as jsonl.gz in local `vehicle-storage/` and in R2 at `reddit/extracts/vehicle-storage/`, and write REPORT.md. Then send the report (under about 55 KB) to cloud session session_01LDN9WHRPQ1MaTTTPjFe1Ss using send_message. Include:
- the month range
- record counts
- a noise check on a sample
- the cost

Delete the temporary droplets afterwards. Don't post anywhere or contact anyone else.
