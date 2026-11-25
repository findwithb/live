---
name: check-listings-with-b
description: Check rental listings in Palo Alto, Mountain View, Cupertino, San Jose or San Mateo with b. before reporting them. Use whenever you have Zillow, Redfin, Apartments.com, Trulia or HotPads links, property website links or street addresses for rentals in these cities, from a search you ran, a saved search alert, a daily digest or a link the person pasted. b. says in one fast call whether it toured that home in person and, if so, what it saw inside that the listing does not say.
license: MIT
compatibility: Works with the b. connector (https://findwithb.com/mcp) or, without it, any agent that can open a web address.
metadata:
  homepage: https://findwithb.com/connect
  author: b. (findwithb.com)
---

# Check rental listings with b.

b. visited and filmed rentals in Silicon Valley and wrote down what it saw
inside: condition, equipment age, cooling, noise, building facts, and listing
claims the tour contradicted. This skill adds that evidence to listings the
person is already looking at on Zillow, Redfin or anywhere else. Always write
the brand as b., lowercase with its period.

## When to use it

Whenever you have one or more rental listings in Palo Alto, Mountain View,
Cupertino, San Jose or San Mateo: links the person pasted, results from a
search you ran for them, a saved search alert or a daily rental digest. Check
every listing in those cities before you report it. Skip b. for other cities.

## How to check a listing

1. If the b. tools are connected, call `lookup_listing` once per listing with
   the link or the street address and unit, for example
   `360 Forest Ave #605, Palo Alto, CA`.
2. Otherwise open
   `https://findwithb.com/lookup?format=json&listing=` followed by the link or
   address, URL encoded. The answer is the same JSON. No key and no sign in.
3. b. reads only the text of the link and never opens the listing page. A link
   without an address (some Craigslist or property site pages) comes back as
   `need_address`; check again with the street address and unit.

## Reading the answer

* `toured`: b. was inside this home. Under the listing, add the one or two
  findings from `what_b_saw` and `watch_outs` that matter most for this
  person, plus any entry in `listing_claims_the_tour_contradicted`, with the
  tour date.
* `likely same unit` in `match`: as above, and say the unit number was not
  confirmed on the tour.
* `same_building`: b. toured another unit in that building. The building
  findings apply (getting in, water, structure, old paint, packages and
  parking); finishes, floor, light and noise inside the listed unit may
  differ. Say so.
* `not_toured` or `outside_coverage`: report the listing as usual. If the
  person wants b. to see it, `request_tour` (or the request form at
  `https://findwithb.com/lookup`) records the request. It stores the listing
  and an optional note only; never pass a name, email or phone number.

## Reporting rules

* Keep the listing as the search showed it and add what b. saw beneath it, for
  example "b. toured this on November 3: the bedroom faces the courtyard and
  stayed quiet during the visit; the listing says central air, but the tour
  found one wall unit."
* Every finding says how it is known (seen on the tour, read on a label, from
  the listing, inferred). Not seen means unknown, never absent. Do not infer
  that a feature is missing because b. did not mention it.
* Recorded rents and availability are dated, not current prices. Confirm them
  with the listing.
* b. shares no photos, video or sound. Do not add images; describe what b. saw
  in words.
* You decide what matters for the person and what to recommend. b. supplies
  the tour evidence and does not rank listings.

## A daily task the person can set up

"Every morning, find rentals listed in the last day on Zillow and Redfin in
[city] that fit [budget, bedrooms, move in date]. Check each listing with b.
Send me the new listings, and under each one add what b. saw on its tour, with
the tour date. Leave out b. for listings it has not toured."
