---
authors:
  - name: null
---

# 7 Depositing to Archives

The following is a short discussion of the tasks required to archive a geophysical survey project. Most of the issues are covered in more detail in the previous chapters (see the references and links below) and only some information is repeated here. The particular tasks depend of course on various factors, like the choice of an Archiving Body, the size of the survey project, already existing practice for in-house archiving and many others. However, most of the time, they can be subdivided into four sections that will be used in the subsequent discussion.
* Planning for archiving
* Geophysical survey
* Creating the Archive
* Depositing to an Archiving Body

## 7.1 Planning for archiving

It is far easier to compile the majority of the Archive incrementally while data are being collected and created than trying to find time at the end for pulling everything together. It is hence recommended to think of folder structure, file naming conventions and databases for metadata even before the start of a survey project. In many organisations there will already be an established procedure for many of these issues but it may be worth reviewing them with a view to making archiving easier.

### 7.1.1 Resources

Most of the tasks involved in creating the Archive are part of a well planned workflow and necessary for creating data backups anyway. Nevertheless it needs to be recognised that archiving has resource implications, most notably in terms of staff time to compile all information, and charges levied by an Archiving Body. Planning for these resources from the outset is therefore essential and may involve applying for grant funding to cover archiving activities and charges, or including archiving in the costing for a commercial contract. In a competitive business environment the challenge is to convince a client that the benefits of archiving outweigh the additional costs. Ultimately, a regulatory requirement for data archiving will be the most persuasive argument. Already, in the U.S. the National Science Foundation requires all grant applications to include a section detailing a ['data management plan'](https://www.nsf.gov/eng/data-management-plans).

### 7.1.2 Folder Structure

As explained in [Section 4.8](archivefiles#id-4-8-file-description), a hierarchical folder structure is well suited to capture the relationship between different files from a project and reduces the required explanatory notes in the File Description Document. In particular the preservation files can easily be linked to the working files in such a structure. In [Section 4.8](archivefiles#id-4-8-file-description) it was suggested to use a template for the hierarchical structure similar to <Project>\<Site>\<Survey_Block>\<Technique>\<Format> (Figure 9). Wherever possible all files created during the project should immediately be stored in this folder structure rather than trying to copy them there at the very end. This also makes it easier to create backup copies while the project is in progress.

```{figure} ../images/g2gp-geophysics-Fig9-Folders-e1652373527551.png
:alt: Figure 9: Hierarchical folder structure

__Figure 9__: Hierarchical folder structure
```

The working files used by the processing software are sometimes kept in folders outside of this hierarchical structure (e.g. C:\GEOPLOT\COMP\<sitename>) and a simple DOS batch file can be set up to copy these files into the project’s folder structure (see Code Snippet 1, below), avoiding pitfalls often encountered when copying files with Windows Explorer (e.g. cmd files may be set to be hidden and forgotten). Such a batch file also allows practitioners to populate the folder structure incrementally as the project progresses, thereby facilitating easy file backup from this storage location.

`SET Sitename=MyProj` (- or whatever is the sitename; it could also be %1)\
`MKDIR Geoplot`\
`FOR %%d in (Comp, Grid, Mesh) DO MKDIR Geoplot\%%d`\
`FOR %%d in (Comp, Grid, Mesh) DO MKDIR Geoplot\%%d\%Sitename%`\
`FOR %%d in (Comp, Grid, Mesh) DO XCOPY C:\Geoplot\%%d\%Sitename%\*.* .\Geoplot\%%d\%Sitename% /S/Y > NUL`

__Code Snippet 1__: DOS batch file (e.g. gpt_copy.bat) for copying Geoplot files for a project into the directory where the batch file resides. Note that the command XCOPY is not available on all Windows installations.

It is good practice to clearly label folders that hold preservation files, for example "Monastic_Granges\High_Cayton\North_Field\Mag\PRESERVE_XYZ". This way the Archiving Body can easily identify files that need to be migrated.

### 7.1.3 File Naming Conventions

It can be difficult to figure out what a particular file 'is' just judging by its name. It is therefore most important to be consistent throughout a project and provide some explanation of the chosen naming conventions. For example a three-letter code can be chosen for a site and all relevant folders or even composites be prefixed with it. Alternatively, the folder structure may contain the site specific code and inside the folder the files can have generic names (e.g. mag, res, 1, 2, 3). Also when composites are saved with data improvement and processing applied they can be labelled with a letter indicating the processing (e.g. 'L' for low-pass filtering) or the processing steps can be numbered sequentially (e.g. 'P01').

It is a good idea to think about this at the start of the project, document it and make the information available to everyone who is working on the project to enhance consistency from the start.

### 7.1.4 Database

Most organisations already have a database in place to record details of the projects they are undertaking. It may be worth considering enhancing such a database with fields from the Comprehensive Documentation discussed in [Section 5](comprehensivedocumentation). It is also conceivable to generate parts of a geophysical survey report directly from the database, either in a tabular form or as a text. Unfortunately, there is as yet no agreed exchange format to transfer the database directly to the Archiving Body's own database and an export as flat spreadsheet is required for inclusion into the Archive.

## 7.2 Geophysical survey

While undertaking the geophysical surveys it is important to take note of items that will be recorded as part of the Comprehensive Documentation [Section 5](comprehensivedocumentation), in particular on land use, soil conditions and instrument parameters. It should also be considered to clearly distinguish between 'survey blocks' (see [Section 4.8](archivefiles#id-4-8-file-description), which are the smallest survey areas for which all measurement parameters are the same and using these to label any intermediate results that are created from the data, for example in the field. The folder structure and naming conventions discussed above should be adhered to from the outset.

## 7.3 Creating the Archive

Although the Archive can be gradually built up following the steps above, usually there will be further work necessary at the end of a survey project to finalise the Archive. To ensure that nothing is forgotten the items listed in [Section 4](archivefiles) could be considered in turn.

### 7.3.1 Working Files

All the files created during the project should be copied into corresponding folders of the hierarchical structure (see above). In particular, proprietary files that were kept in folders allocated by a software package should now be copied into an appropriately named folder within the hierarchical structure (e.g. GEOPLOT – see Code Snippet 1 above). This applies not only to geophysics files but also to all other files, for example GIS, CAD or graphics files. Some of the latter files (e.g. ArcMap mxd documents or svg files) usually only point to the files containing data (e.g. shapefiles) instead of actually incorporating the data. The appropriate folder structure therefore has to be maintained when copying files and if possible relative file paths should be stored (in ArcGIS, for example, this can be selected under File > Document Properties > Data Source Options > Store relative path names to data sources). Care must always be taken to copy all files that belong together, even if they may be hidden from view by settings of the operating system (e.g. cmd files).

### 7.3.2 Preservation Files

A decision has to be made as to which files should be exported to preservation formats and [Section 4.2](archivefiles#id-4-2-preservation-files) provides guidance on this topic. The minimum requirement is to create preservation files for the raw data (i.e. after grid assembly and prior to data improvement) and for the final processed results. However, it is desirable to export all data composites and if possible even all data grids into preservation formats. Preservation files should be created in geophysics coordinates and in map coordinates and stored in appropriately named folders within the hierarchical structure (e.g. PRESERVE_XYZ and PRESERVE_XYZ_MapCoords; tacitly assuming that the former holds preservation files in geophysics coordinates).

It is inevitable that during the export from proprietary formats to preservation formats some information is lost (see [Section 4.2](archivefiles#id-4-2-preservation-files)) and it is hence important to record these metadata separately as part of the Comprehensive Documentation. If not easily expressed in a database, a text document can be used to describe them.

### 7.3.3 Image Files

Image exports should be made from all relevant data and stored in appropriate folders (e.g. called \Images) to show their relationship with the data from which they originate. This includes not only the geophysics composites in geophysics as well as map coordinates but also the GIS and CAD files that are used to convey interpretation of results. While the geophysics data can be pictured well by raster images (tiff, bmp, png; but not jpg!). GIS and CAD file often also contain text and line drawings and are therefore better visualised in open image formats that can represent raster and vector information, like pdf or svg. If geophysics images are created with georeferencing information (e.g. world files or GeoTIFF) other users can easily load them into a GIS environment. Further details about image files can be found in [Section 4.3](archivefiles#id-4-3-image-files).

### 7.3.4 Project Notes

Sometimes not all the information contained on paper-based field notes is easily captured in the electronic files that are created for a project; an example might be sketches of notable features in the survey area. It is useful to scan such records and store them in a suitable electronic format, for example pdf/a (see  [Section 4.4](archivefiles#id-4-4-project-notes)). These can then be put into a folder, for example called \Project\Notes_Scanned.

### 7.3.5 Project Report

Another folder (e.g. \Project\Report) can hold the report that is created for the project ([Section 4.5](archivefiles#id-4-5-project-report)), including the word-processing text file (e.g. doc) as well as a print copy (e.g. pdf). If these were initially stored in a different folder a copy should be placed in the Archive’s hierarchical folder structure.

### 7.3.6 Geophysics And Project Metadata

Some of the geophysics metadata are normally stored in files created by the proprietary geophysics software (e.g. size of data grids, line separation, reading interval) and are therefore incorporated into the Archive as part of those files (see above). However, it is recommended to include this information explicitly into the tables of metadata to make it more readily available. These tables might be created as an export of a database that has been set up to hold such information (see above) or the tables shown in [Section 5](comprehensivedocumentation) could be copied and filled with the relevant information, either as a spreadsheet or a text document, and saved in an appropriately named folder (e.g. \Project\Metadata). As mentioned before, there is as yet no agreed exchange format to transfer metadata directly to an Archiving Body’s own database.

Information on the data processing history is stored in some geophysical processing packages but is not always easy to export. In this case a screen capture of the software’s display of processing steps can help to document these metadata. Otherwise, and for GIS and CAD packages which do not usually track processing, notes on the most important steps should be kept in text documents and saved as additional metadata for the project.

### 7.3.7 Geophysics Georeferencing

As discussed in [Section 4.7](archivefiles#id-4-7-geophysics-georeferencing) georeferencing information is required on three aspects:
* the geophysics coordinate system (procedure used to lay out the grid; where is the coordinate origin; estimates of accuracies for re-establishing the grid),
* coregistration to site grid (coordinates of control points, both in the geophysics coordinate system and the site grid, together with their respective accuracies; geophysics or site coordinates of map-features, if coregistration with a map is required; geophysics or site coordinates of ground features used for georeferencing), and
* georeferencing (description and approximate location of ground features for reference; distance to ground features for key points along the baselines; compass bearings of baselines).

All this can be captured in short text documents with some sketches, either created in a digital drafting package (e.g. InkScape) or in neatly drawn paper documents that are scanned to supplement the textual description. A suitable storage location would be in a folder called \Project\Georeferencing, or alternatively in the folder hierarchy for each respective survey block.

### 7.3.8 File Description

It is not necessary (or even desirable) to create a list of all files that make up the Archive (hundreds or even thousands; Code Snippet 2 shows how to easily create a text file with all file names that can then be shortened). If a clear folder structure has been chosen the logical relationship of the files is immediately clear. Code Snippet 3 (below) shows how a text file with the folder structure can easily be created. This can form the basis for a text document that describes how files are stored in the Archive.

`DIR /S /A-D /ONE /B >fdir.txt`

Alternatively:

`TREE /A /F >fdir.txt`

__Code Snippet 2__: DOS batch file (e.g. fdir.bat) for creating a text file that contains all file names in folders and sub-folders of the current folder (i.e. where the batch file resides). The 'switch' /B ensures that only the filenames are included and can be omitted if more information is required.

`DIR /S /AD /B >ftree.txt`

Alternatively:

`TREE /A >ftree.txt`

__Code Snippet 3__: DOS batch file (e.g. ftree.bat) for creating a text file that contains the folder tree starting from the current folder (i.e. where the batch file resides).

In addition to a listing of the folder structure with a brief description of folder names, some of the file names may need to be explained where meaning is conveyed in the name. An example already introduced in [Section 4.8](archivefiles#id-4-8-file-description) could be if the composite with raw data for a survey block is named with a three letter site code and a two digit number for the survey block (e.g. HCT04) and any data improvement or processing is expressed with a processing label and a running number (e.g. HCT04P08). Any such naming convention needs to be clearly described. It also needs to be identified what are the raw data and what are the final processed data. These could for example be the ones with the highest processing number or they might have a label indicating this (e.g. HCT04F). The location of sites and survey blocks with relation to the georeferencing information also needs to be made clear.

A frequent source of frustration when reusing data is that files may have well known file extensions (e.g. dat, txt) but exactly in what format the information is stored may not be obvious and should hence be explained (more details can be found in [Section 4.8](archivefiles#id-4-8-file-description)).

The guiding principle for including information into the File Description Document should be that a person wishing to re-use the data should be able to make sense of the files and folders without having to open and inspect them all.

## 7.4 Depositing to an Archiving Body
If the Archive has been compiled according to the steps listed above it is ready for archiving. As a first step it can in this form be saved in a secure location for storage. However, to reap the benefits of archiving (see [Section 3](documentingandarchiving)) it should also be deposited with an Archiving Body (see [Section 3.4](documentingandarchiving#id-3-4-the-archive-and-the-archiving-body) for different types). Each Archiving Body will have its own requirements, charging policies and forms to complete. This information can be obtained from the Archiving Body, either through their web site or from the respective data curator. A well-formed Archive as described above will be far easier to 'ingest' (i.e. incorporate) for the Archiving Body and archiving charges may hence be minimised. In particular, the clear indication of preservation files (e.g. through appropriate folder names), which the Archiving Body has to earmark for future migration, helps with the evaluation of a deposited Archive. Only if no quality control and no identification of migration files are envisaged (types 1 and 2 of Archiving Bodies) can such a manual inspection be avoided. Any more advanced Archiving Body will have to recover the associated labour costs.

Important when negotiating with an Archiving Body are Intellectual Property Rights (IPRs). If for example the IPR for data is held by the client of a geophysical contractor deposition of an Archive may require explicit permission of the client. Similarly, decisions will have to be made about data confidentiality if an Archiving Body makes data publicly accessible (type 4). An Archiving Body will usually address all these issues in its deposition policies.