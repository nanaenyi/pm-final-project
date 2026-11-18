# Competitive Analysis & Journey Map (Module 2)

## Responses
- **Role, who are you solving for? (the specific user segment or profile):** Frontline fleet dispatchers at regional delivery and 3PL fleets, who coordinate drivers in real time during the shift. They’re the people who use RouteLogic most heavily, and their usage is falling fastest.
- **Goal, what is this user ultimately trying to achieve?:** To see where every driver really is and push route changes to them instantly, so every delivery gets done on time without chasing drivers outside the system.
- **Friction, the main barrier (moment of misery) stopping them from succeeding:** When a dispatcher reassigns a route, it takes 10 to 15 minutes to reach the driver, with no push notification, so drivers act on outdated routes. Driver status takes up to an hour to show on the dashboard. The dispatcher can’t trust the board, so they run the fleet through a WhatsApp group “as the real system” (UXR-02, UXR-09, BUG-2044, BUG-2072).
- **External tools, the outside platforms or tools the user is forced to use:** A WhatsApp group (the “real system”), text messages from drivers confirming deliveries, and phone calls to read routes back to drivers when the app crashes.
- **The process, the 3 to 5 manual steps the user takes to get the job done:** Reassign the route in RouteLogic, because it’s the official record.
Post the same change in the WhatsApp group straight away, because the app takes 8 to 15 minutes to deliver it.
Wait for the driver to confirm in the chat, and call them if they don’t.
Ignore the dashboard’s status and track real progress from driver texts and messages.
Reconcile RouteLogic with the chat later so the records match. (Steps 3 and 5 are reasonable inferences, not direct quotes from the research.)
- **Core frustration, the exact moment the process feels most “broken”:** The moment right after a reroute. The dispatcher has made the change in RouteLogic, but the driver won’t see it for 10 to 15 minutes and gets no notification. Meanwhile the dashboard still shows outdated status, so the dispatcher can’t tell whether the change landed and has to go to WhatsApp to make sure it does.
- **The evidence, a specific quote or behavior from the research that proves this:** The evidence, a specific quote or behavior from the research that proves this
“I reassign a route and the driver doesn’t see it for ten, fifteen minutes. By then they’ve driven the wrong way. We keep a WhatsApp group as the real system.” (UXR-02, fleet dispatcher). BUG-2044 confirms it: reassignments take 8 to 15 minutes to reach drivers, and the app sends no push notification.
- **Your journey map, a shareable link, or the map file you committed (e.g. journey-map.html):** https://github.com/nanaenyi/pm-final-project/blob/51e3ac0f382aac25d6b1335aec1bb176fbabcf78/02-discovery/routelogic-velocity-future-state-journey.md
