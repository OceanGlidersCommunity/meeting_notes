## background of OGDMTT
* https://www.oceangliders.org/taskteams/data-management/
* formed 2019
* remit to harmonize glider standards from around the globe (currently the US, european and australian standards)
* first major task to harmonize file format
* Been working on this new standard called OceanGliders1.0 format
* We want to cover other standards like QC, metadata, vocabs etc.
* Started with the metadata and making it more FAIR

## leadership and meetings
* Emma and Jenn have taken over from Victor Turpin and Dan Hayes as co-chairs

## news
* Currently the GDAC is not accepting OG1, but it is working on it. Likely early in the new year. (IFREMER)
* Coriolis will provide a script to convert EGO to OG1
* alseamar: will rely on pyglider and coriolis to serve OG1 format.
* the US DAC is working on implementing their solution where they will mediate between the DAC and users, keep taking in data in the same format plus some more metadata
* Haven't heard anything from the eurogliders task team... Didn't get an invite to the SOOP/XBT/IQUoD meeting
* Next March is an IODE meeting in Columbia (Kimmo). Unclear if the call is out yet


## action items
* @Emma Gardner   to talk to BODC team about how vocabs map to netcdf
* add a description of how standard_names are following CF  volunteer?
* why do we have these singleton variables? These will blow up on aggregation... Maybe we should just have one singelton variable that uniquely identifies each datapoint. how about a mission identifier, with the last few bits as the dive number. WIGOS ID has the wmo number and some other stuff related to mission number.  volunteer?
* @Jenn S   to nudge Gui on sharing code for the checker/going open source
* We have PHASE but nothing to identity profile, yo etc. What about the BUFR format? Does it have profile number? Has been specced for glider data now. We should check  volunteer?
* @Callum Rollo  to raise an Issue on defining profile number
* Find out who's in ocean gliders slack that's not in UG2 volunteer?
