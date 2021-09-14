# AgMIP End-User Translation Tools

AgMIP data formats were developed to store and transfer data related to field crop experiments, farm surveys, and other agronomic data in an efficient, flexible format (Porter et al, 2014). AgMIP crop modeling protocols promote the use of multiple models for research applications (Rosenzweig et al, 2012). The AgMIP data products were originally developed to allow data from diverse sources to be harmonized using a common vocabulary, to be combined with expert knowledge, and to be translated equivalently to the model-specific formats used by individual crop models (Figure 1). 

## Data Format

The AgMIP harmonized data format is referred as ACE, or AgMIP Crop Experiment format. These semi-structured AgMIP data are stored in key-value pairs, where the key corresponds to an [ICASA variable](www.tinyurl.com/icasa-mvl) which inherits a definition and a unit. AgMIP data may be available in either JSON or ACEB formats. The JSON (JavaScript Object Notation) suffix is a recognized data formatting standard. Many JSON readers are publicly available and allow easy parsing and processing. The ACEB format, or ACE binary format, is simply a GZipped (compressed) JSON file.  AgMIP has developed tools for viewing ACEB data and for translating AgMIP formatted data to model-specific formats for several crop models.

As shown in Figure 2, AgMIP data files consist of three parts, experiments, weathers, and soils. Relational linkages occur through use of 'soil_id' and 'wst_id' variables. Data sub-structures are used for management event data. For example, in Figure 2, a fertilizer event has been expanded to show date of application, the nitrogen amount applied, and other details. Data sub-structures are also used for soil layer data and for time series data, such as weather or field observations of plant growth characteristics.

## AgMIP Data Tools

AgMIP data interoperability tools can be freely downloaded from the [AgMIP toolshed](http://tools.agmip.org/). The more useful tools for most Ag Data Commons users are:

- [ACEB Viewer](http://tools.agmip.org/acebviewer.php) – This tool allows ACEB files to be explored visually. 
- [QuadUI](http://tools.agmip.org/quadui.php) – This java software application can be run as a desktop application or from a command line. The application reads various data formats, including AgMIP JSON and ACEB files, and converts data to model-specific formats. 