---
authors:
  - name: null
---

# 5 Comprehensive Documentation

## 5.1 Introduction

This section provides a comprehensive list of all relevant metadata fields that can be used to document the project and the surveys undertaken, while Section 6 illustrates some sub-sets that are used in certain archiving environments. These metadata can either be presented in a list (e.g. a text document or spreadsheet) or as a flat database (e.g. in csv text format). It is also conceivable that an XML schema will be developed in future that simplifies the process of metadata compilation and storage.

Several metadata fields may have more than one entry (e.g. *Solid geology*, *Monument period*) and the necessary information can either be provided as a comma separated list in one field (e.g. *Solid geology*: limestone, sandstone) or by repeating the same field several times as separate lines in the list or multiple records in a database (e.g. *Solid geology*: limestone; *Solid geology*: sandstone). A site is often investigated during several 'survey visits', each of which may have encountered very different weather conditions. It is therefore useful to indicate the duration of each such survey visit and then annotate fields where the condition may have changed with the respective survey visits, like *Weather* or *Soil condition* (e.g. *Duration*: 2-25 Mar 2010 (survey visit 1), 10-19 Jun 2010 (survey visit 2); *Weather*: dry after prolonged rain (survey visit 1), prolonged dry period (survey visit 2) ).

It is recommended to make use of existing term lists (sometimes also referred to as 'vocabularies' or 'thesauri') that are appropriate to the country in which the investigation was undertaken, for example for geological terms or monument periods. The term list used should be specified in all cases in the field *Term list*, even if a project-specific term list is defined by the user and provided as a separate file. This section provides some pointers for possible term lists but many more, including automated vocabularies (e.g. the REST based system offered by the British Geological Survey [-@bgs2011vocabulary]), are rapidly evolving as part of the Semantic Web.

## 5.2 Project metadata

Project information gives a spatial and archaeological context to the geophysical data and provides information that could influence their interpretation. This may include information about local geology or the weather conditions on the day of the survey, how the instrument was set up, how the survey was orientated, and where the survey grids were located. While seemingly obvious at the time of the survey, it is essential to record this information as project metadata for future use by the survey team and others.

```{list-table}
:header-rows: 1

* - Field name
  - Description
* - Survey name
  - The name of the site, project or survey. It may either be the name used in a written report (e.g. 'A46 Widening Scheme: Area B') or the familiar and/or published place or monument name where this exists (e.g. 'Stonehenge, Lesser Cursus').
* - Survey index
  - The indentification number/code used internally for the survey and the related area
* - Survey purpose
  - A brief summary (max. 200-300 words) of the main aims and objectives of the project from which the data collection arose and the purpose of the geophysical survey. Possible entries for this field include: 
    * field evaluation in advance of development
    * site management
    * archaeological research
    * technical research
* - Report summary
  - A brief description of the findings of the survey. In many cases this will be the abstract of the survey report.
* - Bibliographic references
  - Relevant bibliographic information about the site or project.
* - Survey keywords
  - Keywords indexing the subject content of the data set. They can be drawn from the fields listed below (e.g. Solid/Drift geology, Monument type, Period, Survey type etc.).
* - Spatial coverage
  - The map coordinates of the SW and NE corner of a bounding box enclosing the survey area, specified with the datum to which they relate (e.g. WGS84; see [Appendix 2: Coordinate Systems](appendix2#a2-2-coordinate-systems).

    In Britain, British National Grid coordinates are recommended and should be given at least to the nearest 100m 'six figure grid reference'. It should be remembered that such map coordinates may be inaccurate (up to several metres), and also that the Ordnance Survey of Great Britain (OS) holds copyright over the reproduction of OS maps and reatins Intellectual Property Rights in all information derived from such maps.

    In the USA, tDAR creates spatial coverage metadata using latitude and longitude (expressed as decimal degrees).

    There may be instances, for example, at sites where there is a threat of looting, where this information must remain confidential (esepcially if access to the geophysical data might lead to criminal activity). In such cases it may be necessary to restrict or omit location information (including clues from which a location can be deduced) from publicly accessible records.
* - Administrative area
  - The District/County/Unitary Authority in which the survey area lies. The administrative boundaries that are current at the time of the survey should be used.
* - State
  - The state, or similar national entity, in which the survey was undertaken. In Germany this would be a Bundesland and in the UK this would be England, Northern Ireland, Scotland or Wales to highlight the relevant archaeological government body.
* - Country
  - The country in which the survey was undertaken.
* - Solid geology
  - The underlying solid geology, including extra information from other quoted sources. All relevant geologies should be listed. A term list is available from the British Geological Survey [-@bgs2011rock], which also provides a REST based automated vocabulary service [@bgs2011vocabulary].
* - Drift Geology
  - Relevant drift geology for the survey area. All relevant geologies should be listed. BGS term lists are as shown for the field *Solid geology*.
* - Duration
  - The dates of the first and last day on which the fieldwork took place. If separate periods of fieldwork are related to the same survey event ('survey visits') they should be listed individually as annotations of the dates.
* - Weather
  - A brief description of weather during fieldwork, with additional reference to previous conditions (e.g. 'dry and hot after a prolonged period of heavy rain').
* - Soil condition
  - A brief description of the soil conditions during fieldwork (e.g. very dry, dry, moist, wet, water-logged, frozen).
* - Land use
  - The land use at the time of the survey. The term used could be drawn from the list given in [Appendix 4.1](appendix4#a4-1-land-use).
* - Monument type
  - A classification of any archaeological monument known to exist at the site or that was revealed during the survey. Uncertainty can be indicated by a '?'. For England use of the period terms listed in the National Monuments Record Thesauri [@eh1999national] is a possibility. The text of the accompanying report should describe how this interpretation has been derived: from existing archives, publications or as an interpretation of the collected geophysical data.
* - Monument period
  - The periods of any archaeological monuments on the site. A relevant term list can be found through @fish2010forum.
* - Scheduled Ancient Monument (SAM) number
  - Any sites within the survey area which have been included on the British Schedule of Ancient Monuments should be identified by their county SAM number. This information is included on the relevant survey licence (e.g. issued by English Heritage) or can be obtained from relevant Local Authority department. Similarly, Digital Antiquity collects metadata of agency identifiers, such as Smithsonian trinomials or National Register Information System numbers (NRIS).
* - Surveyor
  - The name and address of the organisation or individual(s) who carried out the geophysical survey.
* - Client
  - The name and address of the organisation or individual(s) who commissioned the survey. Such information may be confidential and may be withheld in some cases.
* - Depositor
  - The name, address and role of the organisation or individual(s) depositing data related to the geophysical survey.
* - Primary archive
  - The name and address of the organisation or individual(s) holding the primary data archive from the survey.
* - Related archives
  - References to the original material for any data derived in whole or in part from published or unpublished sources, whether printed or machine-readable. Details should be given of where the sources are held and how they are identified there (e.g. by accession number). If a digital collection is derived from other sources it should be indicated whether the data represent a complete or partial transcription/copy, and the methodology used for its computerisation. Also full references to any publications about or based upon the data collection should be provided.
* - Copyright
  - A description of any known copyrights held on the source material.
* - Term list
  - The term list used for the terms in the various fields above.
  
```

## 5.3 Geophysics metadata

Some information about the survey techniques used during a survey is required. This will help to assess the suitability of the archived geophysical results for later re-use. Such information would enable questions such as, for example, 'was the sampling interval close enough to detect narrow and shallow ditches?'

### 5.3.1 All Survey Techniques

The following is a list of fields that are useful to record for each survey technique on each individual survey event. This information may hence be repeated several times to cover all techniques employed on all survey visits.

```{list-table}
:header-rows: 0

* - Survey type
  - The category of geophysical technique used should always be recorded. The following list, while not entirely exhaustive, gives examples of the survey types most commonly encountered in archaeological geophysics:
    * magnetometer survey (land based)
    * magnetometer survey (marine)
    * magnetic susceptibility (volume- or mass specific susceptibility); including random samples, gridded, lab based measurement of samples and field based in-situ measurements
    * earth resistance survey
    * Electrical Resistivity Imaging (ERI); including pseudosections and tomography
    * Vertical Electrical Sounding (VES)
    * electrostatic survey
    * low frequency electromagnetic
    * Ground Penetrating Radar (GPR)
    * seismic
    * microgravity
    * magnetotelluric (MT)
    * Very Low Frequency electromagnetic (VLF)
    * radioactivity
    * Side Scan Sonar (SSS)
    * singlebeam echosounder
    * multibeam echosounder
    * sub-bottom profiler
* - Instrumentation
  - Specific information about the type and configuration of the geophysical instruments used (e.g. specific probes or antennas) is required to assess the information available. As an example, it could be recorded that a 'Bartington Grad 601-2 Fluxgate Gradiometer' or a 'SIR2 GPR system from GSSI with a 400 MHz dipole antenna' was used for a particular survey event.
* - Reasons for choice of survey technique
  - A short statement on the reason why this particular survey technique and its methodology was selected helps with the future evaluation of the survey results. Possible reasons include:
    * archaeological questions
    * previous aerial photographic evidence
    * previous geophysical survey results
    * current land use
    * previous land use
    * underlying solid and drift geology
    * other local geomorphological and topographic factors
    * degree of access to land
    * time, money and personnel available for the survey
* - Area surveyed
  - It is helpful to have an indication of the area of ground covered with each survey technique, as this allows a quick estimate of the quantity of data collected. The unit of measurement used should be clearly stated (square metres or hectares are equally acceptable).
* - Method of coverage
  - To assess the extent of the survey coverage it is important to record the method by which the ground was covered and the data were acquired. Possible methods are (see [Section 2.2](thelifeofgeophysicaldata#id-2-2-data-acquisition))
    * gridded data
    * line data
    * non-gridded data
    * scanning
* - Traverse separation
  - The separation between adjacent __walked survey traverses__ should be recorded in metres where a series of parallel lines (a 'regular grid') is used to collect data for a particular technique. For multi-sensor instruments (e.g. Grad 601-2) a clear differentiation between this separation of traverses walked (e.g. every 2 m) and the resulting Line separation of the merged data lines from the different instruments must be made (e.g. 1 m for two sensors).
* - Line separation
  - The separation of __resulting data lines__ after the merger of all sensor data from a multi-sensor instrument (cf. Traverse separation) should also be recorded.
* - Reading interval
  - If data are recorded at regular intervals along the traverses, the distance in metres between adjacent readings should be noted.
* - Sampling position
  - The exact position where data were recorded, whether within the grid squares or at grid corners (e.g. '0.5m in both directions from the SW grid corner').
* - Data grid size
  - If data were collected over individual data grids, their size should be documented for ease of data coordination (e.g. '20 m x 20 m').
* - Accuracies
  - The accuracy of recording, both in terms of the spatial accuracy (i.e. how well the measuring position matches the assumed recorded position) and of the recorded values (i.e. the level of signal noise). Although a numerical estimate of the accuracy would be useful, it may be sufficient to document the recording method in detail, for example whether automatic or manual triggers were employed, which data range was selected on the instrument, and whether data were collected while moving or stationary.
* - Additional remarks
  - It is important to note any other technical aspects of the survey which may have a bearing, such as instrumentation problems, or the use of non-standard techniques.
```

In addition to these metadata, the following information is required for earth resistance, magnetometer, low frequency electromagnetic surveys and ground penetrating radar surveys. 

### 5.3.2 Earth Resistance Surveys

```{list-table}
:header-rows: 0

* - Electrode configuration
  - The earth resistance response from shallow features depends strongly on the electrode configuration used. It is therefore important to record this information for a thorough interpretation of the results. Examples of possible probe configurations include:
    * twin-probe
    * Wenner
    * equidistant double dipole ('Wenner-beta')
    * general double dipole
    * square
    * Schlumberger
* - Electrode spacing
  - The depth to which features are recorded depends on the electrode separation used, so it is very important to record the distance between adjacent electrodes, for example on a mobile twin-probe frame.
* - Multiple configurations
  - Earth resistance data may have been recorded at each measurement location with different electrode configurations using a multiplexer (e.g. Geoscan MPX15) and information about this sequence should be provided.
```

### 5.3.3. Magnetometer Surveys

```{list-table}
:header-rows: 0

* - Magnetic north
  - The orientation of the geophysics coordinate system relative to Magnetic North is important for the interpretation and processing of magnetometer data and an accurate record should be made. The use of a compass is recommended, as Magnetic North differs from True North and Grid North, and varies slightly with time.
* - Instrument drift
  - The instrument used for the geophysical survey may show a gradual change of its readings with time ('drift'). If information on such a drift is recorded regularly (e.g. after the completion of each grid for an FM256 fluxgate gradiometer) the effect may be compensated by the use of appropriate software. Details of the method used for monitoring the instrument drift and the measured drift itself should be documented (e.g. 'log zero-drift after each grid at common position').
```

### 5.3.4 Low Frequency Electromagnetic Surveys

```{list-table}
:header-rows: 0

* - Coil configuration
  - The distance and relative orientation of the instrument's coils should be specified.
* - Recorded component
  - The recorded electromagnetic component needs to be specified:
    * apparent conductivity
    * apparent susceptibility
    * in-phase
    * quadrature.
```

### 5.3.5 Ground Penetrating Radar Surveys

```{list-table}
:header-rows: 0

* - Antenna information
  - For pulse radar systems, the centre frequency of the antenna, for stepped FM systems the range of frequencies is required.
* - Timing information
  - In order to interpret the results from a GPR survey and to associate the plots with a vertical scale, it is important that information on the time delay for the recording of the first reflection, the time sampling resolution and the maximum time span of the recording are noted. This will allow an assessment as to whether the data provided are investigating deep or shallow ground and what size of features may be detectable.
* - Average subsurface velocity
  - An estimate of the electromagnetic velocity (in m/ns) should be provided to convert two-way travel times to depth. The method used to derive such an estimate should be specified, for example observing ground conditions and using tabulated values, undertaking CMP measurements, a test survey over a target of known depth, fitting of reflection hyperbolas or applying migration tests. 
```

### 5.3.6 Maritime Sonar Surveys

```{list-table}
:header-rows: 0

* - Average water velocity
  - An estimate of the water velocity (in m/s) should be provided to convert two-way travel times to depth. The method used to derive such an estimate should be specified.
* - Sonar frequency
  - The sonar frequency used should be provided in kHz.
* - Beam width at nadir
  - An estimate of the beam width gap in degrees at nadir is required for multibeam echosounders.
```

### 5.3.7 Survey Methodology
It is often useful to describe the survey methodology briefly to help re-assemble the data at a later time. The following should be documented for each survey technique.

```{list-table}
:header-rows: 0

* - Data grid layout
  - If data were collected over individual data grids it is important to know where they are located in the geophysics coordinate system to assemble them into an overall layout. There are two possible approaches to the documentation of such a mesh (see [Section 2.2](thelifeofgeophysicaldata#id-2-2-data-acquisition) and [Section 2.6](thelifeofgeophysicaldata#id-2-6-assembling-data-into-composites)):
    * If all data grids are of the same size, their arrangement can be indicated in a table or spreadsheet using the appropriate file names.
    * For arbitrarily sized grids the geophysics coordinates for each data grid's lower left-hand corner can be supplied with an indication of its size.
* - Data grid size
  - This field has already been included in the section of the general Geophysics metadata, but needs to be recorded separately for each data grid if not all data grids have the same size.
* - Resolution
  - The spacing between measurement points in the x- and y- direction. This information corresponds to the above-mentioned items Line separation and Reading interval but it may be necessary to record it for each grid individually.
* - Survey direction
  - The direction in which the first traverse of the grid was surveyed and where the subsequent traverses are located. If, for example, surveying began in the 'top left' corner of the grid (seen in geophysics coordinates), walked from 'left' to 'right' and then on subsequent lines from 'top' to 'bottom', this could be described as 'survey direction in positive x-direction, subsequent lines added in negative y-direction'.
* - Line sequence
  - The way in which the data grid was walked: in parallel lines always in the same direction (uni-directional), or back and forth (zigzag or bi-directional surveying). This information needs to be recorded as destriping or destaggering of data may need to be carried out at a later stage.
* - Drift value
  - If the instrument used is able to record the drift across a grid (e.g. an FM256), this value can facilitate later drift corrections and may be noted for each data grid individually.
* - Bias value
  - In case the data were stored with an offset value subtracted, it is important to record this information for each data grid.
```

## 5.4 Data treatment

There are many data processing functions available to the archaeological geophysicist (see for example @clark1996seeing, @scollar1990archaeological 488, @gaffney2003revealing, @aspinall2008magnetometry). It should be borne in mind that processing may remove the signature of archaeological features (e.g. linear features parallel to the survey direction may be lost when destriping the data) or introduce artefacts specific to the processing functions (e.g. the introduction of negative halos when applying high-pass filters [@clark1996seeing 151]. It is important to give as much detail about the processing 'history' of a data set for later interpretation. Fortunately, most specialised software packages allow inspection of the history of the processing steps. Such a history, together with information on the computer program used and its version often proves helpful in assessing the alterations that were made to the original data. If details of the processing functions are known, or uncommon software has been used, it is advisable to give more detailed descriptions of the processing or refer to relevant publications. The information on the processing can be provided in a tabular format suitable to the applied tasks (indicated as the field *Data processing*) or as a brief description in a text document. It may be helpful to explain why the individual processing steps were performed and what improvements they brought about.

## 5.5 Report

The project report forms part of the archive (see [Section 4.5](archivefiles#id-4-5-project-report)) and it is useful to provide some basic information also as metadata in tabular form.

```{list-table}
:header-rows: 0

* - Report title
  - The title of the report that has been generated from the results of the survey should be included in the metadata.
* - Report reference number
  - Contractors and researchers should annotate their report with a reference number. This could also be an ISBN, ISSN or DOI.
* - Report author
  - All authors of the report should be listed.
* - Report holder
  - It is important to provide the name and address of the organisation(s) or individual(s) from whom copies of the report, or data, may be requested. Often a copy of the report may be deposited with the relevant council office. In some cases permission may be required from client and surveyor to access the report and this information should be provided here.
```

The summary or abstract of the report is best stored in the project field Survey summary.