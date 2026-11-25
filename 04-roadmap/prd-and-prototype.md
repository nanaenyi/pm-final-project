# B6 Driver Alert Notifications, Simplified PRD (RouteLogic)

**Author:** Me · **Status:** Draft · **Target:** High-Fidelity Prototype · **Persona:** Frontline fleet coordinators at regional delivery and 3PL fleets, who coordinate drivers in real time during the shift. Their goal is to see where every driver is and push route changes instantly, without chasing drivers outside the system.

## 1. The Big Picture
- **Vision:** Every route change reaches the driver in seconds, and the coordinator knows it landed, without opening WhatsApp.
- **Press release:** Today, when a coordinator reroutes a driver, the change takes 10 to 15 minutes to arrive and comes with no notification. By then the driver has gone the wrong way, so coordinators repeat every change in a WhatsApp group they call "the real system."

With Velocity Driver Alerts, a coordinator reassigns a stop in two taps. The driver gets an instant alert and accepts with one tap, and the coordinator sees "Accepted" on the board within seconds. One action replaces the reassign, post, wait and chase routine.
- **Success metric:** Average route assign/reassign time, from 8.2 to 4.0 minutes, with step completion above 71%.
- **Guardrail:** Manager adoption of the Financial Reporting Suite (86%) and manager Reporting CSAT (4.5) must not fall.

## 2. The Details
### User stories
- As a coordinator, I want to reassign a stop to another driver in two taps, so that I can react to changes without leaving RouteLogic.
- As a driver, I want an instant alert when my route changes, so that I don't drive the wrong way.
- As a coordinator, I want to see when a driver accepts a change, so that I don't have to confirm it on WhatsApp.
### Screens to build
- Dispatch board (entry point): drivers with their stops and status, and a "Reassign" button on each stop.
- Reassign and driver alert (feature core): a driver-picker panel, a Confirm button, and next to it a mock driver phone showing the alert with an "Accept" button.
- Confirmation: a board badge such as "Accepted by Sam · 0:42," showing the time to acceptance.
### Functional requirements
- Reassignment completes in 2 taps or fewer from the board.
- The driver alert appears within 5 seconds of confirmation (simulated).
- The alert shows the stop name, address and new position in the route.
- The driver accepts in one tap.
- Each reassignment shows Sent or Accepted on the board, with a timestamp.
- A stop can never be assigned to two drivers at the same time.
### Smart behaviors (Situation → Outcome)
- Driver hasn't accepted within 2 minutes → the badge turns amber, shows "No response," and a "Resend" button appears.
- Coordinator picks the driver who already has the stop → Confirm is disabled, with "Already assigned to this driver."
- Driver is offline → the status shows "Queued," not "Sent."
- Stop is reassigned again before acceptance → the earlier alert is marked "Superseded," and only the latest is active.
### Technical constraints
- No external APIs and no real push service; simulate the alerts.
- No login and no database; useState only.
- Mock data: 5 drivers and about 10 stops.
- One page, with the board and the mock driver phone side by side.

## 3. The Logistics
### Features out
- Compliance-flag alerts
- Full real-time status sync (B11)
- Mobile-first dashboard rebuild (B4)
- AI predictive ETAs (B7)
- In-app chat to replace WhatsApp
### Edge cases & safety guard
- The driver is offline when an alert is sent.
- The stop is reassigned to the driver who already has it.
- The stop is reassigned twice before the driver accepts.
- Never show "Accepted" unless the driver actually tapped Accept.
- Never send an alert without the coordinator confirming.
- Never assign one stop to two drivers.
### Decision log
- I dropped compliance-flag alerts from B6, to avoid alert fatigue and keep the pilot focused on reroutes.
- I used driver acknowledgement instead of full status sync (B11), which gives coordinators confidence in each change within 4 weeks.
### Evals
- Time on task: from Reassign to Accept takes under 30 seconds in the prototype, working towards the 4.0-minute target in the pilot.
- Accuracy: 100% of accepted reroutes show the correct driver and stop on the board.
- Safety: "Accepted" never appears without a driver tap, and no stop is ever assigned to two drivers.

## MoSCoW scope
- **Must:** Reassign a stop to another driver from the dispatch board in 2 taps or fewer; Instant alert on the driver's phone when their route changes; Driver accepts the change with one tap; The board shows each reassignment's status (Sent or Accepted) with a timestamp
- **Should:** Flag reassignments with no response after 2 minutes, with a "Resend" button; Show the time from reassignment to acceptance for each change; Queue alerts for offline drivers and deliver them once they reconnect
- **Could:** Driver declines with a reason; Reassign several stops at once; Custom alert sounds and vibration
- **Won't (now):** Compliance-flag alerts; Full real-time status sync for all driver updates (B11); Mobile-first dashboard rebuild (B4); AI predictive ETAs (B7); In-app chat to replace WhatsApp

---
**Builder hook:** Build a working prototype based on this PRD. Use the User Story as the core flow, Functional Requirements as build constraints, and prioritize speed and clarity over visual complexity.
