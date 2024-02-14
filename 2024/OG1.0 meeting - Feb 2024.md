2024, Feb the 12th

### Attendees
Emma Gardner, Guilherm Pimenta Castelao, Justin Buck, Callum Rollo, Victor Turpin

# Agenda
1)	Review settings, code ownership, reviewers, validation rules.
2)	Sensor information : issue [#119](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/119) – “reconsider groups”. 
a.	Leave group concept for later [#119](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/119).
b.	Update the doc and .cdl consequently. 
3)	PARAMETER as optional: issue [#161](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/161) and [#109](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/109)
4)	TRAJECTORY dimension needed: issue [#130](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/130), [#139](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/139), and [PR #136](https://github.com/OceanGlidersCommunity/OG-format-user-manual/pull/136) 


# Actions
*[list of ongoing actions](https://docs.google.com/document/d/1Tkw3o4PTmHfAwEpIS8uU5nNgbdUlNBLzpR4Nj7DHUiU/edit#heading=h.hjk9ubhio23f)*


# Meeting Notes
## Review settings, code ownership, reviewers, validation rules.
* Code owners can merge PR. 
@glidermann @vturpin @castelao @justinbuck @kerfoot @tcarval @emmerbodc @callumrollo @JuangaSocib

* Admin are in charge of the technical management of the repository:
Guilherme Castelao, Callum Rollo

* Reviewers have the authority to approve change in the document.
Dan Hayes, Emma Garder, Guilherme Castelao, Therry Carval, John Kerfoot, Justin Buck, Callum Rollo

## Sensor information : issue [#119](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/119) – “reconsider groups
We step back from the group concept after Seattle meeting in Oct 2022. This is not reflected in the .adoc file and .cdl.

**Action #7 : These two documents should be updated (@vturpin)**

## PARAMETER dimension issues : [#161](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/161) and [#109](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/109)
PARAMETER and PARAM may be redundant. These may cause impact on ERDDAP distribution. We will downgrade the PARAMETER section into highly desireable to allow smooth implementation. It it recalles that the two variables are useful to link the parameter and the sensor together. When several sensor measure the same parameter (e.g. when comparing sensors for instance) this two elements are needed. 

**Action #8 : downgrade PARAMETER section into highly desireable (@vturpin)**

@emmerbodc has been working on ingesting OG1.0 on ERDDAP. BODC found a way to configure ERDDAP to avoid the impact of the PARAM and PARAMETER. She will share the xml config file to the team.

**Action #3 : @emmerbodc share ERDDAP config file to the group.**

## TRAJECTORY dimension issues

issue [#130](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/130): OG1.0 aim to be a single trajectory file, consequently "trajectory" dimension is not requiered.
@jenseva submitted this issue, @castelao will communicate with here to clarify and report on Github. This trajectory dimension should not be needed.
**Action  #9 : @castelao to check with @jenseva about trajectory dimension and close the issue.**

PR [#136](https://github.com/OceanGlidersCommunity/OG-format-user-manual/pull/136): CF1.10 convention is allowing single trajectory file without a trajectory dimension. As OG1.0 is aim for a single trajectory, then trajectory dimension is not needed.

**Action #10 : Request change in PR [#136](https://github.com/OceanGlidersCommunity/OG-format-user-manual/pull/136) to refer to cf1.10. (@vturpin, @jenseva)**

issue [#139](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/139): No cf1.10 compliance checker is available currently. This issue raise that point. @castelao is working on a compliance checker (cf 1.10) to fit OG1.0 needs.

**Action #11 : @castelao is working on a compliance checker (cf 1.10).**

## other action following meeting discussion
Action #12: In order to progress on the alignment with adoc and cdl, @Emmerbodc – provide ncdump of seaglider and slocum example and @CallumRollo – provide seaexplorer example.


Action #3: In order to progress on ERDDAP configuration for OG1.0, @Emmerbodc – provide XML example and share repo on generating the XML from OG1.0 when development work has been done (scheduled late February)

Action #13: @vturpin – tidy up of documents, archive old cdls to avoid confusion

Action #14: Create list of available .cdl and .nc
  - `spray_minimal_og10.nc`: Minimalist mandatory-only requirements example, with gliders data;
  - `seaxplorer_minimal_og10.nc`: Minimalist mandatory-only requirements example with seaxplorer data;
  - `seaglider_minimal_og10.nc`: Minimalist mandatory-only requirements example with seaxplorer data
  - `slocum_minimal_og10.nc`: Minimalist mandatory-only requirements example with slocum data;
  - `full_og10.nc`: An extended example with recommended and suggested metadata;
  - `BGC_og10.nc`: A BGC example


