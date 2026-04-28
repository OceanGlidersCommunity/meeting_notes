> [!quote] Agenda
>Hello all,
>
>Agenda for vocab meeting :
>Review tickets
>
>Discuss vocab documentation
>
>Please read tickets before the meeting to aid in discussion and proposed solutions. If you have any requests for new vocab concepts or collections please create a ticket here [https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues "https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues")
>
> * [https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/201](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/201 "https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/201") - modes
> * [https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/235](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/235 "https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/235") (Will probably need breaking down first)
> * [https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/255](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/255 "https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/255") - variable for vertical currents derived using flight models
> * [https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/296](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/296 "https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/296") - Variables without a standard_name – pull request - [Pull requests · OceanGlidersCommunity/OG-format-user-manual · GitHub](https://github.com/OceanGlidersCommunity/OG-format-user-manual/pull/297 "https://github.com/OceanGlidersCommunity/OG-format-user-manual/pull/297")
> * [https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/298](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/298 "https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/298") - vocab entry for N_MEASURMENTS
> * [https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/299](https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/299 "https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/299") -duplicate parameters. This is potentially wider than the vocab team and discusses limitation in the NetCDF3 structure.
> * [Update LAT LON LAT_GPS LON_GPS according to NVS definitions by vturpin · Pull Request #269 · OceanGlidersCommunity/OG-format-user-manual · GitHub](https://github.com/OceanGlidersCommunity/OG-format-user-manual/pull/269 "https://github.com/OceanGlidersCommunity/OG-format-user-manual/pull/269")
> 
>Best wishes,
>
>Emma

<u>Participants</u>
* Emma Gardner (BODC)
* Callum Rollo (VOTO)
* Aaron Mau (VOTO)
* Chantelle Layton
* Danielle "Dani" Wright
* Felix Margirier
* Flavien Petit
* Mariarita Caracciolo
* Thomas "Tom" Gardner

Just going through ticket items.
https://cfconventions.org/Data/cf-standard-names/current/build/cf-standard-name-table.html
### 293
Danielle "Dani" picking up issue 293
### 289
CF does not allow spaces in variable names. Sensor names have spaces in them. Callum suggests snake-case. This is also how we link the variable to its sensor. All variable names are all uppercase, so sensors should also be uppercased.

vocab.nerc.ac.uk/collection/OG1/current

Callum picking this one up.
### 298
N_MEASUREMENTS, appears as variable.

Not derived in the format.

Is the number of measurements synonymous with number of timestamps?

Current thought is that it isn't actually measured, and is coming from the dimension of the file. It's in a unique spot as derived metadata and a dimension.

Callum assigned to add a suggested definition.
### 299
Tom introducing this one.

Uniqueness of variable names - CHLA to CHLA2.

Assigning the 2 or 3 suffix based on whichever comes first. Between deployments, no guarantee that one sensor will stay "2".

Felix - vLiz says sensors will always be linked. So this doesn't matter - it will be linked appropriately and well-described. L22 and serial number are appended to the variable, which makes it unique within the OG file.

Seems like we're happy keeping the existing terminology, but we can add changes if BODC prefers (could break some stuff for them).

We have different backscatter wavelengths - could do this for other optical sensors that use specific wavelengths.

Flavien Petit to report back to the group on optical sensors for a future meeting.
### 269
LAT LON LAT_GPS LON_GPS

PR was blocked.

GPS variable didn't match CF standard names. As per issue 296, we have some variables that will probably never get a standard name in CF. We need a flow to ID how to name variables. If we relax requirement for everything to have a `standard_name`, the GPS variables would be OK.

Victor moved on, Gui hasn't been to a meeting in a while. Closing this issue, going to reopen.
### 297
Where available, and not in CF, don't make them mandatory. There are some variables that will never be in CF. So we can't make it mandatory. However, we can propose things to CF.

Callum to put in a PR for this.
### 255
New parameter for derived vertical parameters.

Felix - WG for vertical velocities exists, but it's inactive. Eleanor Frajka Williams and Merckelback have been related to it for a while. Computed variable highly depends on the flight model.

Felix will put in a description for this ticket.
### 235
Felix - can you break this one down?

	Adding a lot of missing vocab items. Victor was asking for things that were missing - mapping sensors that were not included at that point. Many of these are in OG now.

Felix will follow up on this one - he can't remember what Victor wanted it for.
### 201
Pierre asking if there is a data mod. We don't have a vocabulary yet for a data mode.

See `data_mode.md` in the `vocabularyCollection` of the OG-format-user-manual for more information.
Emma will look at this offline - she started writing a document to help know which vocab to use.

Different groups would use a different vocab collection depending on the style of platform they had.
If anyone else has tweaks or changes, just add it to the ticket.

Data mode impacts filename - good to get this done sooner rather than later.
### 290
`long_name` is unstructured. Should be following CF convention, which requires both standard and long. We should define where the `long_name` is from.

We're getting `long_name` from the NERC/NVS variable definition.

Want to comply with CF.
https://cfconventions.org/Data/cf-conventions/cf-conventions-1.7/build/ch03s02.html

We don't state where the `long_name` comes from at the moment.

Callum to put in a PR, assuming `standard_names` are coming from CF and strongly recommended and `long_name` is coming from definition.
### Other stuff
(Not sure where this particular issue is)

`glider_phase` vs `glider_command_phase`: Do we know what the latter means? It was added in 2018 and it isn't clear what it is meant to be used for. It reads like an engineering unit.

Does anyone at BODC know what this represented?

>	"Need to get Justin on the call."

Dani created "identifier of glider phase".

Might need to deprecate glider command phase "GLCOMPH".

Emma to comment that we're going to deprecate it - if we don't hear back in about a month, we'll go ahead and deprecate it. Callum thinks this collection (phase translation tables) can be published.
Dani will make the collection and get it published.
#### nvs-vocabs/OG1 issue 20
https://github.com/nvs-vocabs/OG1/issues
FLUOTURB. There are differences between some sensors - raw fluorescence signal from turbidity sensor. 

All fluorescence-detecting sensors, we should include FLUOR in the name to designate raw or counts vs the scientific value.

If OG1 says something is required, there *must* be a CF definition for it to fall back on. This complicates things like `SEGMENT_NUMBER`.

### Closing
Emma recommends everyone review issues as they show up. Callum can get you added to the notifications list if you like. Emma suggests doing a documentation review soon.

Flavien feels like he would like to meet more frequently but shorter. Callum agrees - the process of walking through the tickets is good.

Mariarita - next time we should discuss versioning. For those that aren't sitting in on these meetings, it's hard for them to stay kept up.