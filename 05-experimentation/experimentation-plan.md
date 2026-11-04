# Experimentation Plan (Module 5)

## Get your documents ready
- **From M3, your hypothesis sentence:** Based on interviews in which users described scrolling for 20 minutes without watching and calling the catalog "a warehouse," plus funnel data showing 71% of visitors never press play, I believe that replacing choice overload with a short, hand-picked Spotlight Curated Rail for the Overwhelmed Browser (Wanderers, 41% of the base) will result in faster viewing decisions, more sessions with playback, and lower first-month churn, as measured by a 15% or greater reduction in median Time-to-Play. I will protect Playback Start Failure Rate and will make a go/no-go decision after 8 weeks against a holdout group, with an early read at week 3.
- **From M3, your primary success metric & guardrail metric:** 15% or greater reduction in median Time-to-Play
- **From M4, the feature you scoped in your PRD this is what you're testing:** A1 Spotlight Curated Rail - Hand-picked homepage rail that bypasses the algorithm

## Define your experiment parameters
- **Feature under test pull from your M4 PRD:** A1 Spotlight Curated Rail: a hand-picked rail of 3–5 titles at the top of the TV home screen that bypasses the recommendation algorithm. A curator refreshes it weekly through remote config, and it has no "See all" link.
- **Persona pull your M2 persona:** The Overwhelmed Browser (Wanderers)
- **Expected outcome the behaviour change you expect, from your M3 hypothesis:** Wanderers who see the Spotlight rail will stop scrolling and leaving. They'll pick a title from the 3–5 hand-picked options and start watching sooner, and they'll come back often enough to stay subscribed past the first month.
- **Primary success metric the one number that defines success, from M3:** Median Time-to-Play: time from app open to a play that lasts 2+ minutes, measured for Wanderers. It excludes sessions that end in a technical failure.
- **Baseline rate today's rate of your primary metric, from your M3 data:** With limited data, I would use this 29% visit-to-play (Snapshot 1) as baseline metric
- **Guardrail metric & boundary what must not break, and how far it can move before you investigate:** Playback Start Failure Rate: % of plays that fail, stall for more than 10 seconds, or return the viewer to the home screen. It must not rise above baseline.
- **Minimum Detectable Effect (MDE) the smallest improvement worth shipping, your floor:** a 15% relative reduction in median Time-to-Play for Wanderers, variant vs. control.
- **Sample size per arm use the calculator in the builder, baseline + MDE:** 161
- **Traffic split & test duration 50/50 standard · cover ≥ 2 weekly cycles:** 50/50 standard over 14 days (>2 weekly cycles)
- **Significance threshold p < 0.05 is standard, explain any deviation:** P<0.05

## Define your control and variant
- **Control (A) the current experience, reference your M2 moment of misery and M3 funnel/workflow data:** She scrolls for about 20 minutes through roughly 15,000 titles, closes the app without watching anything, and ends up putting on a DVD (UXR-01). If she tries to describe what she wants, search fails.  Most visits end without playing anything. 71% of homepage visitors never start a title. That's the "scroll for twenty minutes and close it" behavior from Priya (UXR-01).
- **Variant (B) your single change, copy the relevant screens & functional requirements from your M4 PRD:** Screen 1: Entry Point (TV home screen)
FR-1: The rail contains 3-5 titles. With fewer than 3 valid titles, the rail is hidden. Titles past the fifth are never rendered.
- **Isolation check, what has NOT changed? list everything identical between arms (app version, recommendation engine, notifications, onboarding). If something changed inadvertently, your test is compromised.:** App build	Same TV app version and release train. The rail is switched on by a remote-config flag, not shipped in a separate build.
Devices and platforms	Same eligible TV models and OS versions, including Samsung Tizen 2021+ (BUG-1042) and older TVs with about 11-second cold starts (BUG-1110)
Recommendation engine	Same model, features and ranking for "Because you watched" and Trending (BUG-1091 left as is). No retraining during the test.
Home screen, apart from the rail	Same rows, row order, tile design, artwork and Continue Watching logic. The only layout difference is the added row (see below).
Autoplay	Same trailer autoplay and volume behavior on every non-Spotlight tile (BUG-1077 left as is)
Search and browse	Same search logic (the failed descriptive search stays unchanged, BUG-1080), categories and detail pages
Playback	Same player, CDN, streaming and buffering behavior
Sync and account features	Same My List, resume position and Continue Watching behavior (BUG-1058, BUG-1061, BUG-1121 left as is)
Onboarding	Same signup, profile setup and first-run screens
Notifications and CRM	Same push, in-app and email programs. The Spotlight Digest Email (A6) isn't sent to anyone.
Catalog and content	Same 15,000-title catalog. Rail titles stay available to control users through normal browsing and search.
Pricing and offers	Same plans, trials, discounts and retention offers
Measurement	Same event logging. Time-to-Play is defined the same way in both arms, with technical-failure sessions excluded in both.
Assignment	Randomized by account ID and fixed for the whole test, so one household never sees both arms

## Formalize your hypothesis & shipping criteria
- **Your hypothesis (filled in):** I believe that A1 Spotlight Curated Rail: a hand-picked rail of 3–5 titles at the top of the TV home screen that bypasses the recommendation algorithm. A curator refreshes it weekly through remote config, and it has no "See all" link. for The Overwhelmed Browser (Wanderers) will result in Wanderers who see the Spotlight rail will stop scrolling and leaving. They'll pick a title from the 3–5 hand-picked options and start watching sooner, and they'll come back often enough to stay subscribed past the first month., as measured by a  15% relative reduction in Median Time-to-Play: time from app open to a play that lasts 2+ minutes, measured for Wanderers. It excludes sessions that end in a technical failure. within 14 days. We will protect Playback Start Failure Rate: % of plays that fail, stall for more than 10 seconds, or return the viewer to the home screen. throughout the test.
- **Your shipping criteria (filled in):** We will SHIP if Median Time-to-Play: time from app open to a play that lasts 2+ minutes improves by ≥ a 15% relative reduction in median Time-to-Play at P<0.05 and Playback Start Failure Rate: % of plays that fail, stall for more than 10 seconds, or return the viewer to the home screen does not reach above baseline. We will ITERATE if direction is positive but lift is below the MDE.

We will KILL if the primary metric shows no improvement or moves negatively.

The read date is fixed at the end of 3 weeks, no results reviewed before this date.
- **Hardest parameter to define, and did it change your hypothesis? quick debrief:** The hardest parameter was the baseline for the primary metric, and yes, it changed the hypothesis. Your M3 data has no Time-to-Play baseline. The closest figure is 29% visit-to-play from Snapshot 1, which is a proportion rather than a time. It's also mobile-wide, not TV Wanderers, and it counts any play, not a 2+ minute play. Without a baseline, the target is a 15% relative reduction.
