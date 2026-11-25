# Feature Roadmap, Module 4 · RouteLogic Velocity

**Team:** 2 engineers + 1 designer + 1 CS lead

## Strategic anchors
- **Persona:** Frontline fleet coordinators at regional delivery and 3PL fleets, who coordinate drivers in real time during the shift. Their goal is to see where every driver is and push route changes instantly, without chasing drivers outside the system.
- **Primary metric:** Average time for a coordinator to assign or reassign a route, from 8.2 minutes to the 4.0-minute benchmark, with the step's completion rate rising above 71%.
- **Moment of misery:** When a dispatcher reassigns a route, it takes 10 to 15 minutes to reach the driver, with no push notification, so drivers act on outdated routes. Driver status takes up to an hour to show on the dashboard. The dispatcher can't trust the board, so they run the fleet through a WhatsApp group "as the real system" (UXR-02, UXR-09, BUG-2044, BUG-2072).
- **Guardrail:** Manager adoption of the Financial Reporting Suite (86%) and manager CSAT for Reporting (4.5) must not fall.

## Scoring
| Feature | Value | Effort | Quadrant | Decision | Rationale |
|---|---|---|---|---|---|
| B1 One-Click Compliance Checklist | 2 | 3 | Time Sinker | Later | Exception: biggest time gap in M3 (+11.6 min, CSAT 2.2); likely the next initiative. |
| B2 Smart Daily Report Auto-Fill | 1 | 4 | Time Sinker | Cut | Unrelated to routing, and it risks the Reporting guardrail. |
| B3 Shift Handoff Wizard | 2 | 3 | Time Sinker | Cut | A different step from my metric. |
| B4 Mobile-First Coordinator Dashboard | 3 | 5 | Time Sinker | Cut | Too big; its useful part, 2-tap reassignment, is folded into B6. |
| B5 Step Progress Indicator | 2 | 1 | Fill-In | Next | Cheap, but doesn't speed up route assignment. |
| B6 Driver Alert Notifications | 5 | 3 | Major Project | Now | Exception: the only feature that moves my metric, fixing the 10–15 min reroute delay (UXR-02, BUG-2044). |
| B7 Contextual AI ETA Display | 2 | 3 | Time Sinker | Cut | 1% adoption, and ETAs built on stale status can't be trusted |
| B8 Fleet Analytics Manager View | 1 | 4 | Time Sinker | Cut | A Sales request for managers, who are already satisfied with Reporting (CSAT 4.5). |
| B9 Compliance Audit Trail Export | 1 | 2 | Fill-In | Later | A Legal/CS request; low cost, but no help mid-shift. |
| B10 In-App Coordinator Training | 1 | 2 | Fill-In | Later | The CS lead can train 3 pilot accounts by hand for now. |

## Roadmap
### NOW, Pilot (4 weeks, 3 accounts)
- **B6 Driver Alert Notifications**, Exception: the only feature that moves my metric, fixing the 10–15 min reroute delay (UXR-02, BUG-2044).

### NEXT, GA Release (weeks 5-8)
- **B5 Step Progress Indicator**, Cheap, but doesn't speed up route assignment.

### LATER, backlog
- **B1 One-Click Compliance Checklist**, Exception: biggest time gap in M3 (+11.6 min, CSAT 2.2); likely the next initiative.
- **B9 Compliance Audit Trail Export**, A Legal/CS request; low cost, but no help mid-shift.
- **B10 In-App Coordinator Training**, The CS lead can train 3 pilot accounts by hand for now.

### ✂ Cut List
- **B2 Smart Daily Report Auto-Fill**, Unrelated to routing, and it risks the Reporting guardrail.
- **B3 Shift Handoff Wizard**, A different step from my metric.
- **B4 Mobile-First Coordinator Dashboard**, Too big; its useful part, 2-tap reassignment, is folded into B6.
- **B7 Contextual AI ETA Display**, 1% adoption, and ETAs built on stale status can't be trusted
- **B8 Fleet Analytics Manager View**, A Sales request for managers, who are already satisfied with Reporting (CSAT 4.5).
