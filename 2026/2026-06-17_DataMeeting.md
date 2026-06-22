 ## OceanGliders Data Meeting Wed June 17, 1pm UTC 

https://ucsd.zoom.us/j/92688876982

## Participants 
Jenn Sevadjian, Emma Gardner, Callum Rollo, Aaron Mau, Chiara Monforte, Ellis LaCroix, Jody Klymak, Kristen Sauby

## Focus
OceanGliders updates, existing tools for OG-1.0 and discussing what we can help with in terms of people adopting OG1.0.

## Agenda
### Updates
- OceanGliders data team structure and guidance (Emma, Callum, Jenn)
- New steering team co-chairs, coordinator
- Data task team promoted to Data Team
- Efforts towards international DAC, potential for federated ERDDAP

### OG-1.0
- Versioning, releases (Callum)
- Helper tools (Callum)
  - Compliance checker
  - Data formatter tools
  - Metadata helpers
- Discussion what we can help with in terms of people adopting OG1.0
- Vocabularies working group activity and request for broader group input (Emma)
- Follow-up discussion after vocab meeting (On Monday 15th) with larger group regarding controlled vocabulary for variable names
  - Are we handling duplicate parameters appropriately?
    - At the moment we are creating new vocab terms e.g PRES, PRES2 to handle cases with 2 CTDs on a glider. https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/299
    - Comment from end user regarding best practice to define best sensor - do we use _adjusted channels 
  - When discussing new term "segment" there was not agreement 
    - A few end users would like us to align better to Argo by referring to surface-to-surface as "cycle number". https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/305
    - We need to be careful to avoid confusion with existing term https://vocab.nerc.ac.uk/collection/OG1/current/CYCLEENG/ 

### Future topics:
 - Emma - PHASE, SEGMENT, PROFILE number etc – do we have two terms to describe measured from the platform and then corrected in post-analysis or do we instead use the attribute. Then in the delayed mode version we only keep the best version – something we need to standardise on for the format.


## Discussion, Notes:
- OG Updates
  - Robert Todd and Filipa Carvalho new co-chairs of OG steering team
  - Promoted data management above the task team level
  - Pushing plans for global glider DAC, looking into federated ERDDAP as a solution
  - Starting to ask for plans for delayed mode data and QC'd data as potential next steps for data team
  - Website is getting an update (updating information, fixing bad links)
- Jody asked about potential for harmonizing on gridded delayed mode high quality datasets. Jenn S. and Jody produce this format for their data, not sure if other groups are doing this and/or how applicable it is for broad usage. Potential that this could be a standard data product output of pyglider. Both Jenn and Jody report that this format is the most user-friendly data product they make and that it makes glider data more accessible/usable to non-glider experts. Action:  Jody and Jenn to follow-up.
- Leila BB gave updates on how the US DAC is approaching OG spec. 
  - Have a beta system for taking usual DAC files in combination with json metadata and outputting OG NetCDF. Next step is need users to test it, and would be good for OG data team to provide feedback as well to make sure it meets the spec.
  - Unclear on long-term plans to host the OG formatted files. From OG perspective ideally the US DAC would host OG datasets on ERDDAP so they can be federated to a global DAC. 
- Callum gave an update on tools for OG spec 
  - Jody, Pyglider - Callum and Jody to coordinate on pyglider and OG spec. Potential for community contribution, group effort to update pyglider.
  - Leila - reports potential discontinuities between other metadata standards and OG? To meet other metadata standards some of the OG compliance checks fail?
-Visit github issues for the latest activity on vocabs and to provide input on terms/definitions. https://github.com/OceanGlidersCommunity/
