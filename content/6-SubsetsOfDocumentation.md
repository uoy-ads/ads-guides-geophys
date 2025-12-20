---
authors:
  - name: null
---

# 6 Subsets of Documentation

As mentioned in [Section 3](documentingandarchiving), the Archive consists of three main components: (i) geophysics data, (ii) project material and (iii) project documentation. The latter includes geophysics metadata, geophysics georeferencing, project metadata and file description. The metadata can be thought of as that information that can easily be stored in a database and [Section 5](comprehensivedocumentation) introduces a comprehensive list of metadata fields that are most relevant for the documentation of archaeological geophysical projects. However, some Archiving Bodies store only a subset of these fields in their database or may use slightly different field names, thereby often only offering a subset of the Comprehensive Documentation. In addition, they may insist on the use of particular term lists. When compiling the relevant metadata, for example in an in-house database, it is advisable to start with a fairly comprehensive set of documentation and then 'thin it out' according to what the selected Archiving Body can hold. If the characteristics of these varying practices were captured in XML schemas and RDF vocabularies, automatic translators could be designed to facilitate simple data exchange.

To illustrate subsets of the Comprehensive Documentation it is useful to look at the ADS archive and the ADS ArchSearch database, the OASIS database, and the English Heritage geophysical survey database (EH GSdb). Out of these only the ADS can be considered an Archiving Body as it provides full archiving services for data and metadata, with data migration, preservation and accessibility (Level 4 - Accessible Archiving, in [Section 3.4](documentingandarchiving#id-3-4-the-archive-and-the-archiving-body)). However, its main search interface, ArchSearch, uses only a subset of the metadata (derived from Dublin Core metadata) when facilitating the discovery of the Archive over the Internet. In contrast, OASIS and the EH GSdb use a very full subset of the Comprehensive Documentation but do not store the rest of the Archive, like data files, georeferencing information etc. Table 5 provides the mapping of metadata fields between the Comprehensive Documentation of [Section 5](comprehensivedocumentation) and OASIS, the EH GSdb and the fields used in ArchSearch. Other Archiving Bodies and database holders will also have developed relevant data structures for their databases and mapping these subsets to the Comprehensive Documentation should not pose too much of a problem.





```{list-table} __Table 5__: Mapping of documentation: Comprehensive, OASIS, EH GSdb, ArchSearch.
:header-rows: 2

* - Project Information
  - 
  - 
  - 
* - Comprehensive Documentation
  - OASIS Form Field
  - EHGSdb
  - Dublin Core (ArchSearch)
* - Survey name
  - Project Details: Project Name
  - Project Title
  - Project Title
* - Survey index
  - Project Details: Identifier; Type
  - Survey index
  - Identifiers
* - Survey purpose
  - Project Details: Type of Project; Description
  - Purpose of Survey
  - Description
* - Report summary
  - Project Details: Description
  - Synopsis of report content
  - Description
* - Bibliographic references
  - Project Bibliography section
  - Bibliographic References
  - Relations
* - Survey keywords
  - Project Details: Monument Type; Significant Finds
  - Archaeological Feature Classifications
  - Subject
* - Spatial coverage
  - Project Location: Study Area; Site Coordinates
  - Grid Reference
  - Coverage
* - Administrative area
  - Project Location: District/Unitary Authority; Parish
  - County/Unitary Authority
  - Coverage
* - State
  - Project Location: County
  -
  - Coverage
* - Country
  - (England; Scotland; Wales depending on form used.)
  - Country
  - Coverage
* - Solid geology
  - Project Details - Geophysics: Solid Geology
  - Solid Geology
  -
* - Drift geology
  - Project Details - Geophysics: Drift Geology
  - Drift Geology
  -
* - Duration
  - Project Details: Project Dates
  - Occurred between
  - Dates
* - Weather
  -
  - Weather
  -
* - Soil condition
  -
  -
  -
* - Land use
  - Project Details: Current Land Use
  - Land use
  -
* - Monument type
  - Project Details: Monument Type
  - Monuments covered
  - Subject
* - Monument period
  - Project Details: Period
  - Monument period
  - Coverage
* - Scheduled Ancient Monument (SAM) number
  - Project Details: Identifier (Type = 'SM No.')
  - Scheduled Ancient Monument (SAM) number
  - Identifiers
* - Surveyor
  - Project Creators: Name of Organisation; Project Director/Manager; Project Supervisor
  - Surveyor/Personnel
  - Creators
* - Client
  - Project Creators: Project Brief Originator; Type of Sponsor/Funding Body
  - Client
  - Creators
* - Depositor
  - Project Creators: Name of Organisation
  - Depositor
  - Creators
* - Primary archive
  - Project Archives: Physical; Digital; Paper - all fields
  - Primary archive
  - Relations
* - Related archives
  - Project Archives: Physical; Digital; Paper - all fields
  - Related archives
  - Relations
* - Copyright
  -
  - Copyright
  - Copyright
* - Term list
  - Dependent on Monument / Artefact fields and location of site (i.e. relevant English, Scottish, Welsh lists)
  -
  -
```

```{list-table}
:header-rows: 2

* - Geophysics Metadata
  - 
  - 
  - 
* - Comprehensive Documentation
  - OASIS Form Field
  - EHGSdb
  - Dublin Core (ArchSearch)
* - Survey type
  - Techniques
  - Geophysical Techniques Used
  - Resource Type
* - Instrumentation
  - Project Details - Geophysical techniques: Instrumentation / Instrument Type
  - Instrument Type/Instrument make
  - 
* - Reasons for choice of survey technique
  - 
  - 
  -
* - Area surveyed
  - Project Details - Geophysical techniques: Size of Survey Area
  - Area Surveyed
  -
* - Method of coverage
  -
  - Method of coverage
  -
* - Traverse separation
  - Project Details - Geophysical techniques: Traverse Separation
  - Traverse Separation
  - 
* - Line separation
  - 
  -
  -
* - Reading interval
  - Project Details - Geophysical techniques: Reading Interval
  - Reading Interval
  -
* - Sampling position
  - 
  -
  -
* - Data grid size
  - 
  -
  -
* - Accuracies
  - 
  -
  -
* - Additional remarks
  - Project Details - Geophysical techniques: Notes
  - Comments on Survey
  - 
```

```{list-table}
:header-rows: 2

* - Earth Resistance Surveys
  - 
  - 
  - 
* - Comprehensive Documentation
  - OASIS Form Field
  - EHGSdb
  - Dublin Core (ArchSearch)
* - Electrode configuration
  - Project Details - Geophysical techniques: Resistivity: Electrode Configuration
  - Electrode configuration
  - 
* - Electrode spacing
  - Project Details - Geophysical techniques: Resistivity: Electrode Separation; Electrode Separation Qualifier
  - Electrode separation
  - 
* - Multiple configurations
  -
  -
  -
```

```{list-table} 
:header-rows: 2

* - Magnetometer Surveys
  - 
  - 
  - 
* - Comprehensive Documentation
  - OASIS Form Field
  - EHGSdb
  - Dublin Core (ArchSearch)
* - Magnetic north
  - 
  -
  -
* - Instrument drift
  - 
  -
  -
```

```{list-table} 
:header-rows: 2

* - Low Frequency Electromagnetic Surveys
  - 
  - 
  - 
* - Comprehensive Documentation
  - OASIS Form Field
  - EHGSdb
  - Dublin Core (ArchSearch)
* - Coil configuration
  - Project Details - Geophysical techniques: Electromagnetic: Coil Separation; Frequency; Phase
  - 
  -
* - Recorded component
  - Notes
  -
  -
```

```{list-table} 
:header-rows: 2

* - Ground Penetrating Radar Surveys
  - 
  - 
  - 
* - Comprehensive Documentation
  - OASIS Form Field
  - EHGSdb
  - Dublin Core (ArchSearch)
* - Antenna information
  - Project Details - Geophysical techniques: Ground Penetrating Radar: Centre Frequency of Antennae
  - 
  -
* - Timing information
  - Project Details - Geophysical techniques: Ground Penetrating Radar: Time Window; 
  -
  -
* - Average subsurface velocity
  - Project Details - Geophysical techniques: Ground Penetrating Radar: Average Subsurface Velocity
  - 
  -
```

```{list-table}
:header-rows: 2

* - Maritime Sonar Surveys
  - 
  - 
  - 
* - Comprehensive Documentation
  - OASIS Form Field
  - EHGSdb
  - Dublin Core (ArchSearch)
* - Average water velocity
  - Project Details - Geophysical techniques: Marine - multibeam echosounder: Average Water Velocity
  -
  -
* - Sonar frequency
  - Project Details - Geophysical techniques: Marine - multibeam echosounder: Frequency
  -
  -
* - Beam width at nadir
  - Project Details - Geophysical techniques: Marine - multibeam echosounder: Beam Width Nadir
  -
  -
```

```{list-table}
:header-rows: 2

* - Survey Methodology
  - 
  - 
  - 
* - Comprehensive Documentation
  - OASIS Form Field
  - EHGSdb
  - Dublin Core (ArchSearch)
* - Data grid layout
  -
  -
  -
* - Data grid size
  -
  -
  -
* - Resolution
  - 
  - 
  -
* - Survey direction
  - 
  -
  -
* - Line sequence
  - 
  -
  -
* - Drift value
  - 
  -
  -
* - Bias value
  - 
  -
  -
```

```{list-table}
:header-rows: 2

* - Report
  - 
  - 
  - 
* - Comprehensive Documentation
  - OASIS Form Field
  - EHGSdb
  - Dublin Core (ArchSearch)
* - Report title
  - Project Bibliography: Title
  - Report Title
  -
* - Report reference number
  - Project Bibliography: Other bibliographic details
  - Report Number
  -
* - Report author
  - Project Bibliography: Author / Editor
  - Author/Report Date
  -
* - Report holder
  - Project Bibliography: Place of Issue or Publication
  - Report held by
  - 
```

In addition, the term list used for the field Survey type differs between different organisations, as indicated in Table 6. The mapping between them is straight forward.

```{list-table} __Table 6__: Term lists for the field Survey type
:header-rows: 1

* - Comprehensive Documentation
  - OASIS
  - EH GSdb
* - Magnetometer Survey (land based)
  - Magnetometry
  - Magnetometer
* - Magnetometer Survey (marine)
  - Marine - Magnetometry
  - 
* - Magnetic Susceptibility (volume- or mass specific susceptibility); including random samples, gridded, lab based measurement of samples and field based in-situ measurements"
  - Magnetic Susceptibility
  - Magnetic Susceptibility
* - Earth Resistance Survey
  - Resistivity - Area
  - Resistivity
* - Electrical Resistivity Imaging (ERI); including pseudosections and tomography
  - Resistivity - Profile
  - Resistivity Profile
* - Vertical Electrical Sounding (VES)
  - 
  - Resistivity Depth Sounding
* - Electrostatic Survey
  -  
  - 
* - Low Frequency Electromagnetic
  - Electromagnetic
  - Electro-magnetic Survey
* - Ground Penetrating Radar (GPR)
  - Ground Penetrating Radar
  - Ground Penetrating Radar
* - Seismic
  - Seismic
  - Seismic Refraction
* - Microgravity
  - Microgravity
  - Microgravity
* - Magnetotelluric
  - 
  -
* - Very Low Frequency Electromagnetic (VLF)
  - 
  - 
* - Radioactivity
  - 
  - 
* - Side Scan Sonar (SSS)
  - Marine - Side Scan Sonar
  - 
* - Singlebeam Echosounder
  - Marine - Singlebeam Echosounder
  - 
* - Multibeam Echosounder
  - Marine - Multibeam Echosounder
  - 
* - Sub-bottom Profiler
  - Marine - Sub-bottom Profiler
  - 
```