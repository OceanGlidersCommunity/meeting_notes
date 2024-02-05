2023, Oct the 23rd

### Attendees
Victor Turpin, Guilherm Pimenta Castelao, Kevin O’Brien, Callum Rollo, Emma Gardner

# Agenda
* OG1.0 release
* OG1.0 implementation
* PARAMETER dimension issue
* PHASE variable discussion
* Communication outside the team
* Glider DAC
* New chair

# Actions
*to be updated* *[list of ongoing actions](https://docs.google.com/document/d/1WJ5Q_oTLTUjmutnGOoJUVJ1HLmN7jrI_iQ2VkMK2ipU/edit?usp=sharing)*

## New actions


# Meeting Notes
## OG1.0 release
There was question about whether OG1 has been officially released. There was a communication in June about its release. Discussion was had about a more public release.
The conclusion is that the released should be discussed with the OGST and widerly communicated amongst the glider community.
Action 1: Put the OG1.0 release at the agenda of the next OGST meeting and provide a plan for release. Target is at last June 2024 meeting in Sweden.

## OG1.0 implementation
Emma Gardners group at BODC put together a netcdf file that follows the OG1 format. See the link, but note that only the most recent datasets have been implemented, best to check in with her about getting the proper file. https://linkedsystems.uk/erddap/files/Public_OG1_Data_001/
* One netfd file per deployment and as new data comes it in is appended to that one file.
* With regards to the OG1 netcdf file creation, there were some issues early on with dimensions, but figured it out early on. Tried to follow the CDL on the github page.
* To serve the data, first an internal netcdf is created, then from that a oceangliders netcdf is created. Then the data are served through an ERDDAP FTP, not ingested fully into ERDDAP.
Action 2: Align CDL and format together.
Action 3: How to fully ingest OG1.0 on ERDDAP. Need use case report.

# PARAMETER dimension issue
* John Kerfoot put a github issue 109. https://github.com/OceanGlidersCommunity/OG-format-user-manual/issues/109
* ERDDAP will share variables that have a common dimension but it will only chose one dimension. N_PARAM, N_INSTRUMENTS. So when you serve data normally, any parameters in the n_param dimension won't be served.  Kevin suggested there are workarounds for it but they aren't efficient and involve duplication of variable names. 
* There were a question asked about the utility of the parameter variable. To be inline with the ARGO metadata. The ARGO folks have figured out how to handle this.
This question remain blocking at this stage. A group of us should work on it before official release.
Action 4: Finalize this item with a smaller group to propose something coherent to the community.

# PHASE variable discussion
The OG1.0 format has a phase variable that marks or provides enough information so you can pull out individual profiles. This variable makes getting individual profiles possible with a trajectory (aka timeseries) dataset. Emma asked for phase calculations. John Kirfoot mentioned he had some new code to do this calculation. Adam asked about a published method, but no one on the call spoke up about knowing one. It led to further discussion about the OG community publishing the best method.

The format is design so that the method used to calculate the phase doesn't have to the identified as the best method but must (or should) be published. The idea is to provide the user the information on how the phase has been computed.

# Communication outside the team
-	John is going to give a webinar on the implementation of the OG1.0 from the IOOS glider dac perspective. Some questions he wants to provide answers to are 
-	What is expected for IOOS contributors? Need a really good tight explanation on what it is and how we are going to do it.
-	Once the datasets get there where are they going?
-	What are the benefits?

There is a high need of communication outside the OG1.0 working group.
The impact of the implementation of OG1.0 must be assessed by DAC to identify a timeline.
The benefits to the glider community must be clearly assessed.
The impact on oustide users (data user, data agregarots) should be considered.
The distribution of the data sets into a central hub or an aggregation of distributed center should be agreed amongst the OGDM steering team.

Action 5: work with DAC and data user (agregators) to assess the impact of implementation of OG1.0
Action 6: put at the agenda of next AGDM meeting the organization of the data distribution.

# Glider DAC
-	List of current glider DAC's: BODC, IOOS gliderDAC, Canadian gliderdac, Coriolis, SOCIB (spain), Sweeden glider DAC (VOTO and University of Gothenburg), IMOS.
-	There was some discussion on how to create an serve OG1 files. One method is to use gliderdac in a business as usual sense, but add in the functionality to create OG1 formated netcdf files. In this way, two datasets will be created per glider mission.
-	To create OG1 formated files more information will be needed from data contributors
-	There was further discussion about serving OG1.0 netcfd in ERDDAP or simply through FTP. Some users are going to serve two glider formats, their native one to be used to generate an OG1.0 compatible format.
-	The ultimate plan is for the glider data to be centralized in one central GDAC, but it was unclear who would host the data. Coriolis could be a central GDAC.
-	Creating a second ERDDAP to serve OG1 data requires setup, maintenance, adding datasets to catalog.

This OceanGliders Data Management Architecture discussion should be addressed with the DACs. Today it is unclear toward which objective in terms of global data architecture the group is heading to.

Action: See action 6.



