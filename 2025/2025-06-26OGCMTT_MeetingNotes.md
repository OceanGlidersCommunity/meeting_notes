## OGDMTT vocab meeting 26/06/2025

## Participants 

Callum Rollo,  Robyn Owen, Chiara Monforte, Benjamin Allsup, Flavien Petit, Felix Margirier, Pierre Testor and Juan Gabriel Fernández.

## Discussed topic - Revision of PHASE definition and PR created after last meeting
[https://github.com/OceanGlidersCommunity/OG-format-user-manual/blob/main/vocabularyCollection/phase.md](https://github.com/OceanGlidersCommunity/OG-format-user-manual/pull/279)

After last meeting we all agreed on a definition of PHASE. This definition is based on the engineering commands issued to the glider while it may not always perfectly reflect the glider’s actual movement through the water column.
In this PR, we provide:
1. Improved description of PHASE variable.
2. Improved description of the different phases
3. Included conversion tables and normalization strategy.

## Discussed topic - Segmentation of glider data

Goal of the meeting is to explore how to segment the glider time series data. We need to define the appropriate granularity for segmentation, choose the nomenclature and agree on how to structure and divide the dataset effectively using existing information.

### Proposed Approach

[Segment based on glider PHASE](https://github.com/OceanGlidersCommunity/OG-format-user-manual/pull/276/files)

Advantages
- Easy to compute: relies solely on glider phase.
- Monotonically increasing: no NaNs or unclassified time segments.
- Handles hybrid modes well, like: Multidive sequences; Lateral travel under thrusters during or between dives.

Disadvantages
- Doesn't align with apogee/perigee dive splits.
- Doesn’t define paired up/down profiles (i.e., full dive cycles), which are important for analyses like hysteresis.

### SEGMENT

The group agreed on the suggested definition (SEGMENT_NUMBER starts at 1 at the beginning of a deployment and increments by 1 each time the glider enters the surface phase (PHASE = 3)).

There was no felt need to define a dive cycle (i.e., a paired climb and dive), as this can be easily derived using the PROFILE_NUMBER and profile direction.

One concern was raised regarding the fact that the term "segment" already has an established meaning in the context of Slocum gliders, which differs from this definition. To avoid confusion, it was suggested that we may want to consider adopting a different name for this concept.

### PROFILE_NUMBER

The suggested definition is based on PHASE (PROFILE_NUMBER is 1 at the start of a deployment. PROFILE_NUMBER increments by 1 each time a glider enters a dive or climb phase (PHASE = [1,2]))

Pierre suggested the profile should be defined by vertical motion, to be more useful for science applications. Flavien agrees and Felix suggest we use pressure data from the CTD as the primary source and, if unavailable, using navigation pressure as a secondary option.

The group agreed to combine PHASE and dp/dt to define profiles more robustly. This approach helps to avoid false positives (e.g., bouncing at pycnoclines).

Data collected at the surface will not have a PROFILE_NUMBER assigned and will instead be assigned NaN or a placeholder value (to be decided).

### Profile direction

The group agreed on the need for a variable to indicate the actual vertical direction of the glider (ascent or descent). When combined with SEGMENT_NUMBER and PROFILE_NUMBER, this will allow easy identification of climb-dive pairs (i.e., full dive cycles).

## ACTIONS

### ACTION - Review PHASE PR

If you have reviewing permissions, please check and comment on the [PHASE PR](https://github.com/OceanGlidersCommunity/OG-format-user-manual/pull/279). Once approved, the vocabulary can be submitted to BODC.

### ACTION - Develop algorithms for segmentation and profiling

Everyone should implement an algorithm to detect and split the dataset into phases, segments, and profiles, then validate it using the OG1 datasets. The goal is to find a simple and efficient method for consistent segmentation.

### ACTION - Finalize nomenclature and definitions

Clarify the current terminology and consider renaming "SEGMENT" to avoid confusion with Slocum’s usage.

### ACTION - Next meeting

There are no plans for the next meeting yet. We'll likely reconvene to:

- Review and compare the proposed segmentation algorithms.

- Finalize the chosen approach.

- Decide on the next topic of focus, as PHASE, profile, and segment have been the main areas so far.

