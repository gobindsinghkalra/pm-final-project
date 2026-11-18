# Competitive Analysis & Journey Map (Module 2)

## Responses
- **Role, who are you solving for? (the specific user segment or profile):** Diego, the Frontline Driver
Role: A three-year delivery driver who completes dozens of stops a day, often outdoors and with his hands full.
- **Goal, what is this user ultimately trying to achieve?:** Goal: To confirm each delivery quickly so he can move to the next stop.
- **Friction, the main barrier (moment of misery) stopping them from succeeding:** Friction: In the rain, at a doorstep, with a package in one hand, he must tap through three screens to mark a stop delivered (UXR-01, BUG-2055). He has started texting his dispatcher instead, which means the app is no longer his system of record.
- **External tools, the outside platforms or tools the user is forced to use:** Tools and manual processes
Text messaging to the dispatcher (confirmed, UXR-01). We don’t know whether this is SMS or a messaging app, or what the message contains.
Related channel (confirmed for dispatchers, not Diego specifically): Dispatchers run a WhatsApp group as “the real system” (UXR-02). Diego’s texts likely land in a similar parallel channel.
- **The process, the 3 to 5 manual steps the user takes to get the job done:** Completes the delivery at the doorstep, package in hand (confirmed, UXR-01).
Skips the three-screen “Mark Delivered” flow (confirmed, BUG-2055).
Sends the dispatcher a text saying the stop is done (confirmed, UXR-01).
The dispatcher receives the message and relays or logs it manually (inferred).
The app and dashboard keep showing the stop as open unless someone updates it later (inferred, but consistent with UXR-09 and BUG-2072).
- **Core frustration, the exact moment the process feels most “broken”:** Why the workaround is inefficient
It doesn’t remove the friction. Diego still has to pull out his phone and type, in the rain, one-handed. It trades three taps for a typed message and gives up the structured record.
It doubles the handling. Diego reports the delivery, then a dispatcher has to read it and act on it, which turns a one-person action into a two-person task.
It produces unstructured data. A text carries no reliable timestamp, status, or proof-of-delivery link, and it can’t feed the dashboard.
It compounds the sync problem. Dispatchers already see “in progress” on stops delivered an hour earlier and say they “can’t trust the board” (UXR-09). A text-based side channel makes the board less authoritative.
It doesn’t scale. One dispatcher fielding messages from many drivers becomes a bottleneck.
- **The evidence, a specific quote or behavior from the research that proves this:** How this feeds the business crisis
It erodes the system of record. When drivers report outside the app, the data behind our platform stops reflecting reality, and that damages the product’s core promise.
It undermines the value buyers pay for. Admin reporting is “why we bought it” (UXR-10), but reporting is only as good as the data entered. Off-platform completions mean incomplete reports.
It links the driver problem to the dispatcher problem. Diego’s workaround adds to the dispatcher’s mistrust of the board, so one UX flaw spreads into the sync problem.
It drives the renewal risk. The regional manager ties driver experience to adoption and renewal risk (UXR-10), and the ops manager is evaluating a leaner competitor (UXR-04).
It supports your hook’s message that friction on the core action pushes people off the platform, though the workaround is texting, not spreadsheets.
- **Your journey map, a shareable link, or the map file you committed (e.g. journey-map.html):** https://github.com/gobindsinghkalra/pm-final-project/blob/f8121c89aa6df562815f9ff7947954417d8d11ed/02-discovery/diego-future-state-journey.md
