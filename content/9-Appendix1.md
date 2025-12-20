---
authors:
  - name: null
---

# Appendix 1. Preservation File Formats

## A1.1 XYZ Text Files

'XYZ text files' could more appropriately be called 'XYV text files'. These are text files (usually only using ASCII coding) in which each text line contains the values of the coordinates (X and Y) as well as a measurement value. As these files were initially used with topographic heights as the measurement value ('Z') they became known as XYZ text files but any other data value could be used ('V'). The three values can either be separated by blanks, tabs or commas. If commas are used as separators the file format is often referred to as csv, meaning 'comma separated values'. It can be useful to add a header line to a XYZ text file that contains the names of the columns represented in subsequent lines (e.g. "X, Y, MagField").

The data coordinates X and Y can either be expressed in the geophysics coordinate system, in which case the resulting data will usually have a squared-off envelope aligned with the recording grid. Alternatively, they can be provided in a map coordinate system, for example in the UTM coordinates of a particular zone and the data envelope is then usually at an angle. It is essential to provide some information on the exact coordinate system used.

This file format can be extended to represent 3D data, for example resulting from the inversion of several parallel ERI lines, and would then be referred to as XYZV text file format. In geological geophysics the Z-depth values of such data are often quoted positive when downwards but it is recommend to instead specify downward Z values as negative. This way the data are immediately useable for conventional non geological 3D visualisation packages and the XYZ axes form the usual right-handed coordinate system.

## A1.2 ERI Files

At the moment, there is no standard format for ERI data (Electrical Resistivity Imaging) and a simple text file would best be used, for example in an AMNBV format. In this, after a header line, each subsequent line specifies the location of the four electrodes (for current (A, B) and potential (M, N)) and either the measured earth resistance in Ohms (which could be indicated as R in the header) or the already calculated apparent resistivity in Ohm metres (which could be indicated in the header as rho_apparent). The position could either be specified as the number along an electrode array with the actual position recorded in a separate file (useful for 3D surveys) or as the linear distance in metres along a survey line. See Tables A1 and A2 as examples.


`A_Pos, M_Pos, N_Pos, B_Pos, rho_apparent`\
`0.0, 0.5, 1.0, 1.5, 20.3`\
`0.0, 1.0, 2.0, 3.0, 19.4`\
`…`\
`0.5, 1.0, 1.5, 2.0, 21.1`\
`0.5, 1.5, 2.5, 3.5, 19.2`\
`…`

__Table A1__: A simple ERI text file for a 2D survey with locations specified in metres along the survey transect and data values quoted as apparent resistivity.



`File: ERI2.txt`\
`A_No, M_No, N_No, B_No, R`\
`1, 2, 3, 4,  8.6`\
`1, 3, 5, 7,  4.2`\
`…`

`File: ERI2_Pos.txt`\
`No, Pos_X, Pos_Y`\
`1, 0.0, 0.0`\
`2, 1.0, 0.0`\
`…`


__Table A2__: Two ERI text files particularly suitable for a 3D survey, with electrodes specified by their number, and their actual position provided in a separate file. Measurement values are quoted here as earth resistance but could also be apparent resistivity.


If an inversion process is used to estimate the resistivity distribution related to a measured ERI this can be exported as XYZV text file (see above), where V is the estimated ground resistivity. 

## A1.3 GPR Files
It is strongly recommended to export GPR data to the seismic 'SEG-Y (revision 1)' format as defined by the @segy2002segy. Most GPR packages allow export of their proprietary data to SEG-Y, although not all seem to fully adhere to the SEG-Y standard so it may be best to check the output with one of the free SEG-Y readers available online (e.g. SeiSee, SeiView, SEGYViewer, GSEGYView).

## A1.4 Vector Files
Vector files are best stored as dxf/dwg or as shapefile. More details on these formats can be found in the guides for [Vector Images](https://doi.org/10.5284/xk8x-1e85), [CAD](https://doi.org/10.5284/k5hd-hj61) and [GIS](https://doi.org/10.5284/vk98-3372).