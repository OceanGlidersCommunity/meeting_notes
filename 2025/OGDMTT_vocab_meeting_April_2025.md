 ## OGDMTT vocab meeting 01/04/2025

## Participants 
Emma Gardner, Louis Clement, Callum Rollo, Victor Turpin,  Mariarita Caracciolo, Félix Margirier, Jennifer Sevadjian, Jordan Atherton, Danielle Wright, Filipa Carvalho, Andy Evans 

## Notice
Welcome and introduction from Mariarita Caracciolo, she will be working as Technical Coordinator at OceanOPS. 
This year will be a a transition period as Victor Turpin steps back from OceanGliders program at the end of the year and 
Mariarita joins the program. Mariarita will also be working alongside Laurent Mortier co-ordinating the EGO network.


## Discussed ticket 
https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/272

Heading will have two terms to cover both magnetic north and true north, 
Conversations happening on slack if we need axis mentioning. Updates being made in ticket. 


## Discussed ticket 
https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/278

Oil volume description has to be clear what is meant by positive or negative values  
### ACTION Callum action in ticket to propose preflabel 

Query over if we are including some engineering terms like oil volume why not some others. Agreed to only focus on ones needed to help calculate flight model for now. 

### ACTION Filipa will request some more information from Alex Brearley at BAS who requested this glider speed parameter  

Water velcoities – Louis explained how it works for slocums. Felix explained that for Seaexplorers they do not provide the final version with surface drift accounted for. 
### ACTION Jordan put new definitions agreed upon in meeting into ticket. 

## Discussion points

Whilst discussing new concepts we had some discussion if to include the instrument in the preflabel. Ultimatley we will keep this in to help distinguish when two instruments measure the same phenomena. 
We decided to make it clear in the vocab code if this was not from the best source. E.g. CTD pressure is considered to be the best source and will stay as PRES. 
The pressure sensor used for navigation however is generally considered not as high quality but is useful for scenarios where science sensors are switched off to conserve energy on longer missions. 
Therefore this will be called PRES_ENG. Therefore someone not familiar with glider technology can just pick PRES as this is the higher quality. 

When we have two of the same sensor types measuring the same phenomena we will resort to terms as e.g TEMP2, TEMP3. 

## Discussed adding new vocab collection for PHASE

We also discussed if we were ready to publish a new collection to describe the glider behaviour. 

This lead onto discussions regarding where phase is sourced from, how it is calculated. 
Emma raised that for a DAC it's easier to take from the glider behaviour parameters in the source data but there were concerns about the usefulness of this data given the lag behing sending the piloting command and the 
glider changing behaviour. 

Phase is not easy to calculate but it was agreed that we should look to publish some best practice guidance on the best way to calculate this. 
This will make it easier for a DAC to implement in their RT systems. 

Once this has been established, we can re-look at the vocab collection. 

Need some interested parties to help come up with this guidance for phase calculation. Filipa, Corentin were mentioned in the meeting. 

### ACTION all put forward interested parties to help organise meeting to discuss this further

## Discussion points

It was also discussed if we needed to expand the PHASE collection to include some standardised definitions for the various sections of the glider trajectory e.g some are described in 
https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/273
Because we have the term engineering cycle in the OG1 vocab, there was some confusion if we should be adding them here instead. However there was concern over this as the OG1 vocab is described as 
' Terms describe measured phenomena within the OceanGliders format.'
And these terms are not measured phenomena. 

### ACTION Dani to check if anything exists similar in the NVS and to seek advice from NVS team on how we should proceed i.e. add these into a new collection, or expand the proposed phase collection to include these terms here


