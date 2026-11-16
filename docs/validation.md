# Validation and evidence

This is a record of available evidence, not a new live test run. No automated tests were executed against the current ServiceNow instance for this repository.

| Scenario | Available evidence | Status |
| --- | --- | --- |
| Check in a prepared two-room booking | Front Desk walkthrough: BKG0001124, rooms 109/110, linked occupancy change | Demonstrated |
| Submit room-specific requests | Guest walkthrough followed by two housekeeping requests | Demonstrated |
| Assign, update and complete requests | Housekeeping walkthrough shows ownership, notes/messages and closure | Demonstrated |
| Guest tracking | Guest walkthrough shows the request tracking view | Demonstrated; final post-closure refresh not shown |
| Weather and local discovery | Guest captures show weather and attraction links; export contains integration code | Captured/configured; outage behaviour not tested |
| FAQ and AI assistance | Guest walkthrough includes Wi-Fi help | Demonstrated in original lab; current entitlement/configuration not reverified |
| Room, housekeeping and booking chart drilldowns | Manager walkthrough shows filtered lists | Demonstrated; no fresh count reconciliation |
| Rating and sentiment selections | Manager walkthrough shows filters and matching lists | Demonstrated; current-instance regression not run |
| Checkout and receipt | Active checkout flow and notification in earlier export | Configured; not shown end-to-end |
| Notification delivery | Active notification records and owner-described behaviour | Configuration confirmed; inbox delivery not inspected |
| Guest cannot access another guest's records | ACL/source evidence exists | Live denial test still required |
| Team agent cannot open another team's request | Retained server checks exist | Live denial test still required |
| Stale save and invalid booking dates | Retained editor checks and exported date-validation rule | Negative-path tests still required |
| Sentiment quality | Stored categories appear in manager view | No accuracy benchmark |
| Performance under load | No controlled load measurements | Not measured |

## Before calling it release-ready

Retest the access boundaries using guest and agent personas, including direct record URLs. Reconcile chart counts against filtered lists. Exercise date validation and stale edits. Verify notification recipients and delivery in a non-production environment, then capture the results.

Known screenshot issues include incomplete captures, missing sample dates/prices, an unresolved room reference and inconsistent guest greetings. See [capture notes](capture-notes.md). No numeric performance or business-impact claims are made.
