# Hypothesis & Success Metrics (Module 3)

## Pre-work · Hypothesis check
- **Role , who you are solving for (from M2):** Diego, the Frontline Driver Role: A three-year delivery driver who completes dozens of stops a day, often outdoors and with his hands full.
- **Goal , what this user is ultimately trying to achieve:** To confirm each delivery quickly so he can move to the next stop.
- **Friction / moment of misery , the specific pain blocking their goal:** In the rain, at a doorstep, with a package in one hand, he must tap through three screens to mark a stop delivered (UXR-01, BUG-2055). He has started texting his dispatcher instead, which means the app is no longer his system of record.
- **Current workaround , the external tool or manual process they rely on (M2):** Tools and manual processes Text messaging to the dispatcher (confirmed, UXR-01). We don’t know whether this is SMS or a messaging app, or what the message contains. Related channel (confirmed for dispatchers, not Diego specifically): Dispatchers run a WhatsApp group as “the real system” (UXR-02). Diego’s texts likely land in a similar parallel channel.
- **Problem Hook , your one-sentence framing of the business crisis (M1):** We must solve the risk of losing our largest enterprise account and our position as the market’s most capable operating system by addressing the daily friction that is pushing dispatchers out of the product and into spreadsheets, because every feature built for the 5% is now slowing down the 95% who need to act in seconds
- **Value Proposition , the outcome your initiative promised to deliver (M1):** The new value: RouteLogic Velocity makes the product fast for the people running the fleet today, and keeps every enterprise capability intact for the people who need it. In practice:

A dispatcher-first default experience. The home view is built around live fleet status, exceptions, and the three or four actions that make up most real-time work (reassign, reroute, notify, confirm). Everything else gets out of the way.
Progressive disclosure for advanced capability. Compliance, financial reporting, and specialized workflows move behind role-based views and an on-demand layer. Administrators and executives keep full power, and dispatchers stop paying a tax for features they never touch.
Evidence-based pruning. Each feature is audited against usage data and research, then sorted into four buckets: core (keep front and center), role-specific (show only to the right roles), advanced (on demand), or legacy (retire or sunset).
A speed commitment we can measure. For example: time to complete a reassignment, clicks to the live fleet view, and the share of dispatch decisions made inside the product versus outside it.

## Read your data snapshots
- **Does the funnel data confirm your M2 friction point, or does it tell a different story? Note where the numbers align with the qualitative pain you found and where they diverge.:** _(not filled in)_
- **Do the retention patterns align with the workaround your M2 persona used to find content? Note what the Mo. 0→1 drop suggests about the onboarding experience your persona described as frustrating.:** _(not filled in)_
- **Does the LTV gap and the content mix (61% trending for Wanderers) confirm the moment of misery your persona described? Note which segment your persona is in and whether the data confirms their pain.:** _(not filled in)_
- **Does the low adoption confirm your persona is burdened by tools they don’t use? Note whether the low scheduling adoption (42%) for coordinators matches your M2 moment of misery.:** e scheduling figure (42% for coordinators) isn’t tied to Diego or to any moment of misery in our research. It is a candidate for the “role-specific” bucket, pending evidence that it causes friction.
- **Does the workflow data match the manual process or hack you documented in M2? Note whether the specific drop-offs or time gaps explain why your persona avoids the digital tool.:** No. This snapshot doesn’t match Diego’s hack and can’t explain why he avoids the app. It measures coordinators (our dispatchers), and Diego is a driver. It does supply the first quantified evidence for your hook’s claim that dispatchers are being pushed out of the product.Where it does and doesn’t connect to Diego

No direct match

Nothing here measures Mark Delivered, the three-tap flow, or driver texting. The snapshot starts at “Open RouteLogic” and stays on the coordinator side.
Diego’s misery is physical and situational (rain, one hand, a doorstep). A coordinator at a desk doesn’t face that, so the time gaps don’t explain it.

Plausible but inferred links

Diego’s texts land on a coordinator who must relay or log them by hand. That would add load to a workflow already about 30 minutes over benchmark. This is a hypothesis, not data.
Route Assignment takes 8.2 min vs. 4.0. That is consistent with drivers overriding the optimizer (UXR-05) and the optimizer ignoring closures (BUG-2068), but the snapshot doesn’t say why it’s slow.
The drop-offs show coordinators leaving the in-product workflow. They don’t show where they go. Your hook says “spreadsheets,” which our research never evidenced, and this data still doesn’t confirm it.

New and not in our synthesis

No interview or bug report mentions compliance friction, yet Log Compliance Checks is the biggest gap (14.6 vs. 3.0 min). Snapshot 1 also flagged compliance as high-friction for drivers, who use it at 64%. It may sit in Diego’s flow too, but we have no driver-side data on it.
Numbers to correct before presenting
“69% abandon after Route Assignment” is mislabeled. 71% reach Route Assignment and 31% complete Shift Handoff, so 69% is the cumulative drop through the handoff stage. Only 18% reach the daily report, so 82% never file it.
The biggest single-step drops are two 23-point falls: Fleet View to Route Assignment (94% to 71%), and Route Assignment to Compliance (71% to 48%).
The time gaps sum to 29.8 minutes, not 31. The snapshot attributes 31 minutes to NPS data, so they may be separate measures. Compliance is the largest single contributor at about 39% of the gap, not the whole of it.
Unknown: whether average times are only for coordinators who reach each step. If so, later steps are measured on a shrinking group.
What this means for your persona choice

The strongest quantified evidence is now on the coordinator side, while Diego’s evidence is qualitative (UXR-01, BUG-2055). Your value prop is dispatcher-first too. I’d suggest adding a coordinator persona whose moment of misery is the compliance-heavy, abandoned end-of-shift workflow, with Diego as the supporting driver story.
- **Look at the CSAT heatmap. Which specific cell most directly maps to your persona’s friction? Note how the NPS trend justifies the urgency of your M1 Problem Hook.:** Which cell maps to Diego’s friction?

No cell maps cleanly, and the closest one points the wrong way.

Drivers × Core Dispatch (4.3, Strong) is where Mark Delivered would most likely sit, and it contradicts UXR-01 and BUG-2055. Plausible reasons: the cluster average hides one bad flow, the cluster means the dispatch board or optimizer instead of delivery completion, or drivers like Diego who bypass the tool aren’t rating it. Whether Mark Delivered belongs in this cluster is the first thing to confirm.
Drivers × Compliance (2.8, Weak) is the best-supported weak cell among features Diego actually uses (64% adoption in Snapshot 1). If compliance steps sit in his delivery flow, they would add to his friction. That link is unverified.
Drivers × Scheduling (1.9) and × Reporting (1.1) are Critical but come from features drivers barely touch (15% and 3%). Low ratings from low usage are weak evidence of a “tax” on drivers. They may reflect irrelevance or tiny samples.

The heatmap fits coordinators far better than Diego.

Coordinators × Compliance (2.2) lines up with the 14.6 min vs. 3.0 min gap and the 48% completion in Snapshot 2.
Coordinators × Reporting (1.3) lines up with only 18% filing the daily report.
Coordinators × Scheduling (2.6, Weak) now gives some evidence of dissatisfaction, so it shouldn’t be treated as simply “role-specific” without understanding why.

Correction to the snapshot’s “critical signal”: Compliance and Scheduling are not the lowest clusters for the frontline. Reporting is lowest for both drivers (1.1) and coordinators (1.3). Compliance is actually the second-highest-rated cluster for drivers.

How the trend justifies urgency of your Problem Hook
Coordinator NPS: +18 to a 30-point collapse. The current value printed as “, 12,” so I’m assuming -12. Confirm that before it goes in front of executives.
Time lost: 31 min vs. ~9 (3.4×). This quantifies the manual-workaround drag your hook describes.
Complexity as churn reason: 4 of 5 accounts vs. 1 of 8. This is your strongest support for the “losing accounts” claim, but the samples are tiny and the denominators differ. It also still doesn’t identify a “largest” account.
Manager CSAT is high (Reporting 4.5, Compliance 3.9) while the frontline is low. This supports the split between buyers and users, and your promise to keep enterprise capability intact.
The “dispatchers” claim now has support. NPS and workflow data are coordinator-side. Still, nothing here supports “5% / 95%” or “spreadsheets.”

Velocity pilot (+34% route-assign speed): It supports the hypothesis, but it’s one metric with no sample size. It’s also ambiguous whether it means a 34% time cut (about 5.4 min) or a 1.34× rate (about 6.1 min). Either way it likely stays above the 4.0 benchmark, and it says nothing about compliance or Mark Delivered.

## Step 3 · Craft your hypothesis
- **Qualitative evidence (from M2) , quote the specific friction / moment of misery for your persona:** “I reassign a route and the driver doesn’t see it for ten, fifteen minutes. By then they’ve driven the wrong way. We keep a WhatsApp group as the real system.” (UXR-02). A second dispatcher adds “I can’t trust the board” (UXR-09). Bugs BUG-2044 (8-15 min propagation, no push) and BUG-2072 (20-60 min status lag) back this up.
- **Quantitative evidence (from M3) , name the metric or data point that confirms the pain; cite the number:** 31 min/day lost to manual workarounds, vs. ~9 two years ago (3.4×).
Route assignment takes 8.2 min vs. a 4.0 benchmark (+4.2 min).
Coordinator NPS shows a 30-point collapse (current value assumed -12; confirm).
- **Persona , role, goal, and the friction you confirmed in the reconciliation steps:** Role: A fleet coordinator (dispatcher) at a mid-size 3PL who reassigns routes and monitors drivers live.
Goal: To redirect drivers instantly and trust the live board without a side channel.
Friction: Reassignments reach drivers 8-15 minutes late and the board lags 20-60 minutes, so the coordinator keeps a WhatsApp group alongside the product.
- **Problem you are solving , one sentence describing the specific friction this initiative removes:** Coordinators can’t act on or trust the live fleet state inside RouteLogic, so they run real-time dispatch through manual side channels.
- **Strategic outcome , what behaviour change do you expect, and how does it map to retention / revenue / churn?:** Behavior change: Dispatch decisions move back into the product and out of WhatsApp.
Retention and churn: This targets the “complexity” churn reason, cited by 4 of 5 accounts vs. 1 of 8 before, and the renewal risk raised in UXR-10 and UXR-04.
Revenue: No revenue data was provided, so I can’t size it. Add the ARR of at-risk accounts.
- **Primary success metric (initiative signal) , the leading indicator that tells you the gap is closing:** Median time to complete a route assignment or reassignment. The baseline is 8.2 min, and the benchmark is 4.0. As a companion, track the share of dispatch decisions made in-product vs. outside, but that has no baseline yet.
- **Guardrail metric (product signal) , the metric that must NOT drop; it protects your existing base:** Manager CSAT for Reporting (4.5) and Compliance (3.9) must not fall, because managers are the buyers (UXR-10). Also watch compliance-check completion, currently 48%.
- **Decision window , how much time or data before you scale, pivot, or kill? minimum threshold to proceed?:** These are suggested starting points to validate with your team:

Weeks 1-2: Establish the in-product decision-share baseline.
Weeks 3-8: Run the pilot expansion with accounts that cite complexity.
Scale if median route assignment holds at 5.0 min or less for two consecutive weeks, in-product share rises, and guardrails hold.
Pivot if speed improves but workaround time doesn’t, which would point to sync, not UI.
Kill or diagnose if results fall well short of the +34% pilot gain or any guardrail drops.
- **Draft your full hypothesis sentence , one to three sentences; quote the metric, name the persona, name the outcome:** Based on a coordinator’s account that reassignments reach drivers 10 to 15 minutes late, so “we keep a WhatsApp group as the real system” (UXR-02), and on 31 minutes a day lost to manual workarounds, with route assignment taking 8.2 minutes against a 4.0-minute benchmark, I believe that giving fleet coordinators a dispatcher-first default view will bring dispatch decisions back into RouteLogic and halt the 30-point NPS decline, as measured by a 34% reduction in median route-assignment time (8.2 to about 5.4 minutes). I will protect manager CSAT for Reporting (4.5) and Compliance (3.9) and will make a go/no-go decision after eight weeks of pilot data.
The 34% target is borrowed from your Velocity pilot result. If “+34% speed” means a 1.34× rate rather than a 34% time cut, the target would be about 6.1 minutes, so check how the pilot defined it.
The eight-week window is my suggested placeholder. Adjust it to how quickly you can gather pilot data.
The outcome is stated as returning decisions to the product. It’s not yet measurable, because there’s no baseline for in-product decision share. Capturing that baseline early would let you turn the outcome into a second metric.
A dispatcher-first view won’t change the 8 to 15 minute delay in reaching drivers (BUG-2044). If that sync issue isn’t in scope, the WhatsApp workaround may persist even if assignment gets faster.
