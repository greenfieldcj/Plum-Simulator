Plum 360 Simulator
A web-based simulator of the ICU Medical Plum 360™ infusion pump, built for nursing education and new-device orientation. Runs in any browser — laptop, iPad, or phone. No install, no account, no app store.
Live site: https://greenfieldcj.github.io/Plum-Simulator/

What it is
A faithful (but unofficial) simulation of the Plum 360 pump's interface and programming workflow, designed for high-volume practice before learners touch a real device. The simulator covers the menu tree, drug library navigation, dose calculation, soft and hard limit handling, primary and secondary line programming, titration, bolus delivery, and selected alarm states.
What it's for

Nursing students learning IV pump programming for the first time
Experienced nurses transitioning to the Plum 360 from another pump platform
Clinical educators running orientation, competency check-offs, or skills lab practice
Faculty looking for a low-cost rehearsal tool that scales beyond the one or two physical pumps available in a typical lab

Two modes
The simulator launches with a role picker:
Student mode — All three tiers visible with Tier 1 (Pump Familiarization) expanded by default. Step-by-step scenario descriptions. No time pressure; passing requires completing the steps correctly.
Experienced Nurse mode — Tier 1 collapsed (still accessible). Clinical scenarios surface first. Terse scenario descriptions. Time benchmarks shown next to each scenario. The verdict grades on three levels: mastery (gold star — pass under benchmark with zero errors), complete, or not yet complete.
The scenario library (29 scenarios across 3 tiers)
Tier 1 — Pump Familiarization (9)
Mechanical interface skills. No clinical complexity.

Power on the pump
Stop a running infusion
Program a simple rate
Correct an entry with CLEAR
Acknowledge a VTBI Complete alarm
Find a drug in the library
Backprime the cassette
Recover from a hard-limit rejection
Titrate a running infusion

Tier 2 — Basic Floor Scenarios (10)
Common med-surg and ED workflows. Familiar drugs.

NS maintenance fluids
D5W maintenance
LR for fluid resuscitation
Switch maintenance fluid (NS → D5 1/2 NS)
Cefazolin IVPB
Ampicillin IVPB
Morphine basal infusion
Furosemide drip
Diltiazem (a-fib rate control)
Labetalol drip

Tier 3 — Critical Care & Complications (10)
ICU starter pack plus complication response.

Heparin (continuous, weight-based)
Norepinephrine
Dopamine
Epinephrine
Propofol (sedation)
Insulin drip with titration
Vancomycin piggyback
Nitroglycerin
Hydromorphone basal + bolus
Heparin + distal occlusion (complication response)

Features

Tap-and-go interface — every pump button is mapped to a click/tap zone. Works identically on touchscreen and mouse.
Drug library with soft/hard limits — programs that exceed soft limits prompt for override; hard limits cannot be overridden.
Real-time delivery simulation — accelerated time scale (~20 seconds per scenario VTBI) so students see delivery, alarms, and titration without waiting for real-world infusion times.
Per-student progress tracking — results saved in browser localStorage. Completed scenarios show best time and date. Tier-level completion summaries shown in the sidebar.
Event logging — every keypress, state transition, error event, and decision point is timestamped in a visible log. Useful for student self-review and for educators reviewing what went wrong on a failed scenario.
Mastery thresholds — each scenario has a time benchmark for the experienced-nurse mode. Three consecutive mastery-level runs of a scenario is a defensible threshold for clearing a learner to real-device practice.

How to use it

Open the live site URL on any device with a browser.
Enter your name and pick a role.
Pick a scenario from the sidebar.
Press [ON/OFF] on the pump face to start.
Work through the scenario.
On completion, the verdict shows your time and any errors. Click "Try it →" to move to the next scenario, or pick a different one from the sidebar.

Progress is saved per name in the browser. Coming back later? Enter the same name and your completed scenarios will show with checkmarks. Switching between two students on the same device? Click "Change" at the top of the sidebar.
What this is not

Not a substitute for hands-on lab time on a real pump. Button feel, screen visibility, mounting on an IV pole, and physical line management are skills only the real device can teach. The simulator handles the cognitive load (menu trees, sequence, dose calculation, alarm response) so the hands-on session can focus on what only the hands-on session can teach.
Not validated by ICU Medical. This is an independent educational tool. Drug library values are illustrative and modeled on typical ICU practice, not Cottage Health System's actual MedNet library.
Not for clinical use. Practice only. Never use this simulator to determine actual patient infusion programs.

Built with
Pure HTML, CSS, and JavaScript. No frameworks, no build step, no external dependencies beyond Google Fonts. The entire simulator is a single index.html file.
State management is a hand-rolled finite state machine — every screen on the pump is a state, every user action is a transition. Adding a new scenario means adding an entry to the SCENARIOS config object; the engine handles the rest.
Version history

v0.4 (current) — Mode toggle (Student / Experienced Nurse), 29 scenarios across 3 tiers, mastery-level grading with per-scenario time benchmarks
v0.3 — Three-tier scenario organization, name entry, per-student progress tracking
v0.2 — Eight scenarios across all major workflows (heparin, norepinephrine, NS, insulin titration, vancomycin piggyback, nitroglycerin, hydromorphone bolus, occlusion complication)
v0.1 — Single heparin scenario, MVP state machine, event logging

Contributing
This is a single-developer educational project. Issues and suggestions welcome via the repo's Issues tab. The most useful feedback is from clinical educators and students actually using the tool — what's confusing, what's missing, what's wrong.
Credits
Built by Christian Greenfield, MSN, RN, CCRN, CNE. Clinical Nurse Coordinator at Cottage Health System; clinical nursing faculty at Westmont College's ABSN program.
The Plum 360 interface is modeled on the publicly available ICU Medical Plum 360 System Operating Manual (part 430-98340-004). All screen layouts and behaviors are rendered from scratch in CSS; no proprietary assets are used.
License
No license currently set. If you'd like to use this in your own institution's teaching, open an issue or reach out — happy to discuss.
