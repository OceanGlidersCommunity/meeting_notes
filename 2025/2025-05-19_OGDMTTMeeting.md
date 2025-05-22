 ## OGDMTT vocab meeting 19/05/2025

## Participants 
Emma Gardner, Louis Clement, Callum Rollo, Mariarita Caracciolo, Félix Margirier, Jordan Atherton, Filipa Carvalho, Chiara Monforte, Pierre Testor, Benjamin Allsup, Flavien Petit

## Notice
Callum Rollo is the new chair while Emma Gardner is away for maternity leave. 

## Discussed topic - Improvement to the glider phase table
https://github.com/OceanGlidersCommunity/OG-format-user-manual/blob/main/vocabularyCollection/phase.md

### Phase Definition

The phases described here refer exclusively to the time when the glider is at sea. They do not include any phases, states, or behaviors associated with the glider while it is out of the water (e.g., simulation dives).

Each phase is intended to represent the engineering state of the glider, i.e what the glider is attempting to do, rather than what it is physically doing. 
For example, a "descent" phase refers to the glider trying to descend, even if it is actually stalling or failing to do so.

Since this distinction may not always be scientifically relevant, there has been discussion about introducing an additional variable. This new variable would describe the glider’s actual behavior or state, regardless of it is trying to achieve.

### Propelled and parking phase

There was a discussion about whether propelled ascent and propelled descent should be treated as separate phases. 
It was agreed that they should not be distinguished—whether the glider is using only ballast or also propulsion during ascent or descent. The use of the propeller during these phases can be inferred from other variables.

It was also clarified that the "propelled" phase should be reserved for horizontal/lateral movement only and not for vertical motion. This distinction should be made clear in the phase description.

Regarding the "propelled" and "parking" phases: while both involve no significant vertical movement, they should not be merged. 
The engineering intent is different—during parking, the glider is attempting to maintain position with the motors off, whereas during propelled, the motors are on and the glider is attempting to move horizontally.

As a result, both definitiosn should be adjusted. The "propelled" phase should clearly indicate horizontal/lateral movement. The "parking" phase should specify that the glider is attempting to hold position with no lateral movement.

### Numbering order

The possibility of assigning more meaningful numbering to the phases was discussed. It was confirmed that the current numbering is arbitrary, with phases 1, 2, and 3 being the most commonly used. 
The use of 0 is the only convention with a specific rationale, as it represents the 'unknown' phase.

### Unknown phase

The need for an 'unknown' phase was discussed and confirmed. It is necessary to always assign a phase, even when no other defined phase is suitable. 
In such cases, 'unknown' serves as a fallback and ensures that no other phase is incorrectly used as a default.

### Ascent and descent

There was a discussion about whether "ascent" and "descent" phases should be defined based on actual depth changes or based on the glider’s intended (engineering-driven) behavior—i.e., what it is trying to do. 
Defining these phases solely based on depth can lead to issues, especially when the glider stalls or bounces on the pycnoclines. For any derived variables, it makes sense to adopt a more general and simple definition of ascent and descent.

It was agreed that defining phases based on the engineering intent is more appropriate. However, from a scientific perspective this approach may raise questions, particularly around how to classify inflection points. 
This is considered a separate issue and will be addressed later, when we will discuss to what profile the inflection should belong to.

 The current description of the "ascent" and "descent" phases should be updated to reflect intent, using terms like "trying" or "attempting" to ascend or descend.

### Naming the variable phase or behavior

There was discussion about whether "behavior" might be a better term than "phase" to describe what the glider is doing. 
"Behaviour" could more accurately capture the glider’s activity or intent, especially when distinguishing between what it is attempting versus what is actually happening.

However, the term "phase" is already used in the published version of the manual. Changing it now might lead to confusion or inconsistency, so it may not be good to switch terminology at this stage.

Ultimately, the long_name in the metadata is descriptive enough so it should be clear enough what the variable refers to.

### Surfacing

There was a discussion about whether we should distinguish between the surfaced state—when the glider is at the surface, performing communications, GPS fixes, etc.—and the surfacing phase, when the glider is moving toward the surface after an ascent. 
One idea was to use the GPS fix as a defining marker for when the glider has fully surfaced. However, for now, we have decided not to separate these two and to treat them as part of the same surface phase and keep the name 'surfacing'.

### Inflection

The current definition of the inflection phase, as well as its relationship to the transition phase, was considered too ambiguous. 
There was discussion about whether we should remove the inflection phase altogether, and instead use only the transition phase. 

In the end, it was decided to keep the transition phase, but a clearer definition is needed to avoid overlap or confusion with the inflection concept.

## ACTIONS

### ACTION - Add a header description
Callum to add a header clearly stating that the listed phases refer to what the glider is attempting to do, based on its engineering state, and not its actual physical motion (i.e., not reflecting observed vertical or horizontal movement).

### ACTION - Adjust the each phase description 
Callum to revise the wording in the 'phase' table to reflect the emphasis on engineering intent—what the glider is trying to do, not necessarily what it is physically doing.

### ACTION - Glider model phase translation table
Emma to publish the table with the 'translation' of the phases for the different glider models. Callum/Felix/Chiara to add a column for the SeaExplorer.

### ACTION - Next meeting
Callum to send out a poll to schedule the next meeting. He will also open a ticket and share a draft solution for the profile split issue.
All participants should take note of how they handle profile splitting at their institution to prepare for a group discussion at the next meeting. 
