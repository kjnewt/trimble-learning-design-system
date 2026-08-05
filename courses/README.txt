THE RESISTANCE LAB (STORYLINE WEB OBJECT)

HOW TO ADD IT IN STORYLINE 360
1. Extract this ZIP. You will get a folder named "Resistance_Lab" with index.html inside it.
2. In Storyline, go to Insert > Web Object.
3. Choose the "file on a local computer" option and browse to the extracted "Resistance_Lab" FOLDER (select the folder, not the file). Storyline uses index.html as the start page automatically, so do not rename it.
4. Set the web object to display inline (not in a new window) so learners stay in the flow.
5. Recommended web-object size: at least 1100 x 700. The activity is tall, so a near-full-slide object works best.
6. Publish as SCORM and test in your LMS (or SCORM Cloud) rather than relying on Storyline preview alone.

WHAT WAS FIXED IN THIS VERSION
1. Launch bug: two button handlers used the reserved words "continue" and "return" as identifiers, which stopped the entire script from parsing, so nothing on the page responded. Both now reference the buttons safely.
2. Freeze risk in the LMS: the save step called browser storage without a guard. Inside a sandboxed web-object frame that call can fail and previously would have halted the screen change. Saving is now wrapped so a blocked frame can never freeze the experience.
3. Removed all em dashes from the content.
4. Hardened the sound (AudioContext) call so older browsers cannot throw.

FEATURES
- Open Sans with Arial fallback
- Trimble branding
- Name, avatar, and accent color personalization
- Randomized answer order with plausible, similar length distractors
- Customer reaction before coaching
- Trust, openness, momentum, and defensiveness meters
- Three sequential EAR(C) missions
- Print or Save to PDF report
- Downloadable EAR(C) field guide
- Start Over control on Mission Control that clears the rep, avatar, and all mission progress (two taps to confirm, so it cannot be triggered by accident)
- Replay Mission on the results screen for retrying a single mission without a full reset

NOTES ON TRACKING AND PERSISTENCE
- Progress is stored in the browser (localStorage) so a returning learner keeps their profile and unlocked missions. If the LMS frame blocks storage, the experience still runs fully for that session; only cross session memory is skipped.
- Scores are NOT written back to Storyline variables or reported to the LMS. If you need this activity to mark complete, drive completion from the Storyline slide or block itself (for example, a Next button or a slide visited trigger). If you ever need the mission score tracked in Docebo, that is the point at which the questions would be rebuilt as native Storyline interactions.
