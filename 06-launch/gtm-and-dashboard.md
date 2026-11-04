# GTM Strategy & Success Dashboard (Module 6)

## Get your prior work ready
- **The feature you're launching from your M4 PRD, one feature, not a list:** Screen 1: Entry Point (TV home screen)
- **What your M5 experiment told you shipped / iterating, the evidence behind the launch:** The experiment clarified what we need to prove before shipping: does a short, curated rail help Wanderers start watching faster without disrupting playback? The qualitative research and cohort data justify testing the feature, but no A/B results have been reported. The launch decision remains pending the fixed 14-day read.
- **Your persona pull your M2 persona, this anchors your audience:** This engages the Overwhelmed Browser and Wanderers because they are current customers and need a better way to have them start using the product.

## Set your goal, then your audience
- **Primary GTM goal awareness · engagement · conversion, pick one:** Engagement
- **Why this goal? what makes this the right goal for this feature right now:** Because the priority is for them to use the product they have subscribed to start watching the offered titles to them
- **Target audience the specific segment your goal implies, be precise:** This engages the Overwhelmed Browser and Wanderers because they are current customers and need a better way to have them start using the product.

## Size your launch
- **Launch tier S (minimal) · M (targeted) · L (multi-channel) · XL (full GTM):** M (targeted)
- **Justification reach + revenue impact + what silence would risk:** The M (Targeted - focused comms) is the best tier because it's smaller focus for better control with low effort to observe the true impact of the feature. It doesn't involve too many changes so that you can identify the effectiveness of the feature.
- **Is this a launch or a release? does it need go-to-market, or can it just ship?:** This is a controlled release first. The homepage rail is its own discovery mechanism, so it can ship to the test audience without a marketing campaign. We will consider an M-tier targeted launch after validating its impact on engagement.

## Choose your top three channels and plan assets
- **Channel 1 owned / earned / paid, and why it reaches your audience:** Owned - Streamline's TV home screen. The “Spotlight · This Week” rail in row 1 reaches Overwhelmed Browsers and Wanderers at the exact moment they struggle to choose. It presents five hand-picked titles without requiring users to open an email, follow an ad or leave the app
- **Channel 2 owned / earned / paid, and why:** Owned - targeted email to low-engagement subscribers
Email reaches Wanderers who rarely open the app and would otherwise miss the homepage rail. A short message featuring the week’s curated picks gives them a reason to return without presenting another overwhelming list.
- **Channel 3 owned / earned / paid, and why:** Owned - opt-in mobile push notifications. A short reminder such as “Five hand-picked titles for tonight” can reach low-engagement Wanderers without requiring them to open the app or check email. Keep notifications infrequent and aligned with the weekly refresh to avoid adding noise.
- **Enablement & assets what Sales / CS / Support need, plus the assets to build (one-pager, demo, etc.):** Keep enablement lightweight for the controlled release. Sales teams need awareness as new engagement feature and need a one-page internal brief. CS/Support teams need explanations and FAQs with response templates. The content/curation team needs a dedicated owner and a curation checklist with weekly publishing schedule. Product/Engineering team need to confirm eligibility, feature flag requirements and disable options, which is provided by a release checklist including a monitoring and rollback runbook.

## Make it executable
- **Ownership named owner per key activity, individual, not department:** Need a named owner for each activity: 
Experiment brief/ship decision, TV rail implementation, Instrumentation and release safety, Experience design and demo, Weekly content selection, Support readiness, Internal brief and stakeholder updates, Post-validation email and push
- **Budget & resource gaps what costs extra, and any asset you can't currently build:** Extra costs are: 
Weekly curation: editorial time to select five titles, check availability and refresh the rail.
Analytics support: help establishing the baseline, sizing the experiment and analyzing results.
TV testing: devices or testing services if the team lacks access.
Email and push delivery: only after validation, if existing tools and campaign support cannot cover it.
What can't be completed are: 
A validated experiment dashboard: blocked until telemetry and analytics support are confirmed.
Live email and push campaigns: drafts can be built, but delivery tools and ownership remain unconfirmed.
A sustainable weekly content schedule: requires a confirmed curator.
- **Timeline Phase 1 beta → Phase 2 launch moment → Phase 3 post-launch:** Phase 1: Beta (Weeks 1–3: build and readiness. Weeks 4–5: 14-day A/B test.)
Phase 2: Launch moment (Week 6, conditional on beta results)
Phase 3: Post-launch (Weeks 7–10 and ongoing)

## Define how you'll know it worked
- **Success metrics 2 to 3 metrics that match your GTM goal:** Spotlight adoption rate: % of accounts shown the rail that start a Spotlight title and watch for at least 2 minutes
Success metric	Definition	Target / timingSpotlight adoption rate	% of accounts shown the rail that start a Spotlight title and watch for at least 2 minutes	Establish a beta baseline, then measure improvement after launch
Median Time-to-Play: Time from app open to the start of a title subsequently watched for 2+ minutes
Repeat Spotlight use: % of first-time Spotlight viewers who return and watch another Spotlight pick within 7 days
- **Bad signal to watch for e.g. high reach, zero signups = message-market mismatch:** High Spotlight visibility, but few qualified plays and little repeat use. Wanderers see the rail but still don’t choose, suggesting the picks or presentation aren’t reducing choice overload.
Faster starts, rapid abandonment: Time-to-Play improves, but viewers quickly quit. The rail speeds up decisions without delivering satisfying choices.
Strong first-week use, weak returns: Adoption spikes, then fades. The feature may be a novelty rather than a habit.
More playback failures: Interest exists, but technical friction prevents viewing. Investigate reliability before changing the message or picks.
- **Most likely post-launch decision double-down · iterate · pivot · deprioritize, and what would trigger it:** Iterate. This is a planning assumption, not an experiment result.
Trigger: Wanderers try Spotlight, but median Time-to-Play improves by less than the 15% target, or repeat use fades after the first week, while playback reliability remains stable.

Action: Test changes to the picks, refresh schedule or rail placement one at a time, rather than adding more features or expanding promotion.

Double down only when the rail delivers a sustained, statistically supported improvement of at least 15%, alongside repeat engagement and no playback regression. An inconclusive result should prompt further investigation, not an automatic kill.
