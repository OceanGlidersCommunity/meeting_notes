# IUGC June 2024 Data Management Workshop 

-Dan Hayes
-Emma Gardner
-Victor Turpin
-Callum Rolo 
-Justin Buck 
-Alvaro Lorenzo 

Several break out sessions took place to get wide ranging feedback on the following topics  

## The release and adoption of the OG 1.0 data file format: its role and future development (e.g. including technical data, more generic data types like sound, imagery, vectors). How can the OGDMTT help? (Dan)

What about adding new parameters? 
An example is turbulence data. 
Step 1: Are the parameters in the vocabulary? Emma should be able to point people in the right direction.

raw data on platform...on board processing. final data published normally....raw data (10 KB/s) on a site for archival. Currently, PIs do this, and the manufacturer (but limited time period). Should be public probably....

Spectra of shear could be saved with meta data about how it was computed from raw data.

Parameter of interest is dissipation rate profile...if something odd..can go back and look at spectra on GDAC.
Best practice about method used/followed to derive spectra. raw data at PI? or sent to a DAC?
--look into how to storage. L0, L1...which level does OG want? 
--erddap does back up
-SCOR group for the spectral computations in general...ADCPs, microstructure...
-connect with OG best practices to add info about operations.

Each OCG network has a list of EoV...where are microstructure parameters? currents?

Analysing Ocean Turbulence observations to quantify mixing (ATOMIX) SCOR WG160
International Science Council----

Maybe other TT can be made in OG (BP WG for microstructure)...they will contact DMTT to help at some point...

USV...common data 

OASIS---community air-ocean interaction...

AUV——some missions (or parts of missions) may be relevant to GOOS and OceanGliders. Why not use OG1.x?

Summary:
Vocabulary should be investigated, and the method to request additions (if needed) be made known to those who want to add parameters.
The best practices for that parameter should be established, or at least coordinated so that there is consensus about metadata to include, parameters to be EOVs, and to define levels of processing. (L0, L1, … like satellite products). The WG or TT on best practices could also define what Level(s) is for GDAC, for PI, or other archival.
Other platforms like USVs and AUVs have much in common, and could take advantage of OG1.x for GOOS-relevant activities. There are few/no known efforts to harmonize in those fields to our knowledge.

 



## A strategy for delayed mode workflows (PI – DAC – GDAC), how to feed other repositories such as EMODNet. (Victor)



## The role of open-source tools to leverage data management knowledge and capacity across communities. Updates in technology such as federation or cloud services. (Callum)

### What attendees want

- Looking for open source software that can easily process data
- Want to use community standards
- Need a script to transfer from current datastypes (raw data or e..g EGO) to OG1
- Tools need to be more user friendly. How to improve beginner experience
- Tools should be easier to find
- Don't want to reinvent the wheel
- Want small tools that work well for set tasks. Not monolithic workflows
- Want a script that Just Works (at least on a test dataset)

### Attendees concerns

- unclear ownership of SOPs. Fear on stepping on toes if contributing
- Lack of institutional support for open source/SOP activity. All done in free time
- Still using matlab, how to ease the transision to Python
- Some complex toolboxes fail due to being out of date/poorly docuemented/too complex/platform dependant
- Should we worry about speed? Use more e.g. julia
- Formats evolve, tools do not keep up
- Some packages grow too bloated - hard to find relevant parts of code
- Where should we sent the data? Coriolis? EMODnet? copernicus?

## The harmonization underway for command and control (C2) systems for mixed model and mixed mode fleets. Future plans and priorities. (Alvaro)




## Break out on quality control and quality assurance (Justin)
QA/QC covers different levels
Real time automated QC to remove gross outliers for operational oceanography community (Real-rime/R-mode). Data downloaded from platform is another version of this and is known as recovery mode.
Automatically adjusted data for known issues e.g. pressure or oxygen correction based on sea surface values  (Adjusted/A-mode)
Climate grade data after human inspection and calibration (Delayed mode/D-mode)
Mixed (M) mode would cover a deployment
This does not correspond cleanly with existing data sate indicators used in Felds like satellite products but does map to with other networks like Argo. This is a topic that could be looked at the the Ocean Coordination Group for cross network harmoinsation.
 
The need for guidance materials on QA/QC was clear with OceanGliders acting as a facilitator to connect users to guidance. Re-establishing a community manager would be highly beneficial as a community manager would act as the bridge between users and glider best practices/guidance. Such a person would eb a facilitator, communicator and motivator within the community to reinitiate and sustain the best practices and development of guidance in the OceanGliders communicator.
 
The guidance should also extend to the overall data workflows and data assimilation approaches to take account of factor such as time of day or night.
 
The new glider data assimilation task team are keen to work across task team to progress the work collaboratively.
 
How to reduce the delays in the submission of delayed mode data to DACs was discussed. This is for a number of reasons including immature delayed mode methods and apprehension by PIs that the data are not finished/perfect. Guidance is needs to document the expectations on delayed mode process and the QC level of data with intermediate versions possible that include the provenance to ensure any reuse it within the bounds of what would eb acceptable at the intermediate data state



### Not covered 
The potential funding opportunities that could support the above, and the value proposition we can bring: can we describe costs of not proceeding on the above qualitatively or quantitatively? Can we clearly identify improved FAIRness for each improvement made? (Justin)
The role and further specification or development of controlled parameter vocabularies for glider scientific and technical data. (Emma) 
Prioritization and organization of efforts to address the above, or any other topic brought by the attendees, and how OGDMTT may help in the short (1 year) and long (5-10 year) time frame. (?)

