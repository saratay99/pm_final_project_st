# PRD & Prototype Sprint (Module 4)

## Pick & scope with MoSCoW
- **The “Now” feature I’m scoping (name + one-line core description):** A1 - Spotlight Curated Rail: Hand-picked homepage rail that bypasses the algorithm
- **My finalized Must-Haves (after overriding the AI):** M1: One curated rail, limited to 3–5 titles. The limit is the feature. With more titles, it's just another row in the "warehouse." M2: Placed in the first or second home row and visible on TV without scrolling. If users have to scroll to find it, the 20-minute scroll still happens. M3: Selecting a title starts playback in no more than 2 actions Getting from the pick to playback quickly is what reduces Time-to-Play. M5: Only titles that are available and playable for that region and device are shown. A pick that can't be played adds more frustration and hurts the Playback Start Failure guardrail.
- **What I demoted from Must → Should/Won’t, and why:** M6: Built for the TV app first, using remote focus states rather than hover. TV is where the persona browses and gives up. Hover doesn't exist on TV. Could be steep technical overhead to configure for TV version. 
M4: Picks can be updated through remote config, without an app release. Without this, the picks go stale, users learn to skip the rail, and it adds to the clutter. May require larger technical lift to enable and sync with app profile

## Generate your Simplified PRD
- **One thing my PRD makes explicit that a vague brief would have missed:** The PRD explicitly states the hard limit of 3-5 titles that guides the build from engineering. Instead of a vague brief that generalizes the feature without details for testing and validation.

## Prompt-to-prototype sprint
- **Where did the prototype reveal a gap in my PRD logic? (what I had to update):** The Spotlight rail should appear on top of homepage regardless of a previous subscriber or a New subscriber
- **My prototype, as a link or a screenshot (publish or share from your tool; in Lovable that is Share → Share Preview, in Bolt Publish → Web. No share URL? Screenshot the working flow):** https://lovable.dev/preview/KJGZWjU3JdCY0U3cWVFg0NsZEShwN01Q
