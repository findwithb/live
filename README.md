# b.

b. connects Claude to the homes b. has visited and filmed in Silicon Valley: Palo Alto,
Mountain View, Cupertino, San Jose and San Mateo. Claude can search the toured homes, read
the recorded facts for one unit, compare units, check a listing link or street address
against the tours, and look up timestamped moments from each walkthrough, described in words.

Every fact states its basis: seen on the tour, read on a label, from the listing, or
researched. Recorded rents and availability are dated, not a live market feed. b. shares
no photos, video or sound clips, and it does not book visits, take applications or
payments, or sign leases.

## What this plugin adds

* The b. MCP server at `https://findwithb.com/mcp`. No account or sign in is needed.
* Skills that tell Claude how to use the tours well.

## Data and services

* The `check-listings-with-b` skill can check a listing without the connector by
  opening `https://findwithb.com/lookup?format=json&listing=` with the listing link or
  street address. That endpoint is run by b. on the same server and answers the same way.
* Tool inputs are used to answer and then discarded. The one exception is `request_tour`,
  which stores the listing address or link, its city, an optional note (emails and phone
  numbers removed) and an optional date, with no name or contact details.

## Links

* Documentation: https://findwithb.com/connect
* Privacy policy: https://findwithb.com/privacy
* Support: hello@findwithb.com
