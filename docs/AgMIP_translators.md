# AgMIP End-User Translation Tools

AgMIP data formats were developed to store and transfer data related to field crop experiments, farm surveys, and other agronomic data in an efficient, flexible format (Porter et al, 2014). AgMIP crop modeling protocols promote the use of multiple models for research applications (Rosenzweig et al, 2012). The AgMIP data products were originally developed to allow data from diverse sources to be harmonized using a common vocabulary, to be combined with expert knowledge, and to be translated equivalently to the model-specific formats used by individual crop models (Figure 1). 

## Data Format

The AgMIP harmonized data format is referred as ACE, or AgMIP Crop Experiment format. These semi-structured AgMIP data are stored in key-value pairs, where the key corresponds to an [ICASA variable](www.tinyurl.com/icasa-mvl) which inherits a definition and a unit. AgMIP data may be available in either JSON or ACEB formats. The JSON (JavaScript Object Notation) suffix is a recognized data formatting standard. Many JSON readers are publicly available and allow easy parsing and processing. The ACEB format, or ACE binary format, is simply a GZipped (compressed) JSON file.  AgMIP has developed tools for viewing ACEB data and for translating AgMIP formatted data to model-specific formats for several crop models.

As shown in Figure 2, AgMIP data files consist of three parts, experiments, weathers, and soils. Relational linkages occur through use of 'soil_id' and 'wst_id' variables. Data sub-structures are used for management event data. For example, in Figure 2, a fertilizer event has been expanded to show date of application, the nitrogen amount applied, and other details. Data sub-structures are also used for soil layer data and for time series data, such as weather or field observations of plant growth characteristics.

## AgMIP Data Tools

AgMIP data interoperability tools can be freely downloaded from the [AgMIP toolshed](http://tools.agmip.org/). The more useful tools for most Ag Data Commons users are:

- [ACEB Viewer](http://tools.agmip.org/acebviewer.php) - This tool allows ACEB files to be explored visually. 
- [QuadUI](http://tools.agmip.org/quadui.php) - This java software application can be run as a desktop application or from a command line. The application reads various data formats, including AgMIP JSON and ACEB files, and converts data to model-specific formats. 

## Example of translation for DSSAT Cropping System Model using QuadUI

Two sample data files are referenced in this document to illustrate how the AgMIP tools can be used to translate an ACEB file to DSSAT model format (as an example for model inputs). 
NOTE: Other modeling formats can be selected through the QuadUI interface, although (user beware!) some of these translators have not been maintained and may only work for older versions of that model. Please contact the model developers and it@agmip.org if you need an updated translator.

The sample data used in this example are a subset of data for a field crop experiment conducted in Maricopa, Arizona, USA called the Hot Serial Cereal experiment (Kimball et al, 2016). The sample data files referenced herein are:

- [HSC-sample_4.5.aceb](https://github.com/agmip/json-translation-samples/blob/master/Wheat_HSC_SHORT/HSC-sample_4.5.aceb?raw=true) – AgMIP format file, ACEB format with experimental data collected in the field, including metadata, crop management, observations of crop growth and development, weather, and soils data.

- [Field_overlay_HSC_v4.5a.zip](https://github.com/agmip/json-translation-samples/blob/master/Wheat_HSC_SHORT/Field_overlay_HSC_v4.5.zip?raw=true) – DOME file to supply additional information required for modeling.

Figure 3 shows a screenshot of the QuadUI desktop application after a user has selected the HSC-sample_4.5.aceb file. (Note that QuadUI can also be used to translate raw data from Excel and other formats, where providing soils and weather data separately may be convenient, but in this case, the weather and soils data are included in the ACEB file.)

<!-- ![image](https://github.com/agmip/ARDN/raw/master/docs/images/QuadUI.png) -->
*Figure 3. QuadUI screenshot*

The user has selected to translate the data to DSSAT format. When the “Convert” option is selected, the data are translated to DSSAT format. Multiple crop modeling options may be selected simultaneously, and the model input files are created in separate folders for each model. In this case, a single folder for DSSAT will be created for the translated files.
When a user tries to run a simulation with the DSSAT files created, the model will generate errors because a few required model parameters are not present in the data collected in the field experiment. At this point, we need to introduce a separate data source that can supply these additional model parameters, determined or estimated by the modeler.

## DOME files

When the end use of a dataset involves crop modeling, we often find that even detailed descriptions of experiments lack data required by a model. For example, perhaps the type of fertilizer or the row spacing was not recorded. A DOME (Data Overlay for Multi-model Export) file can supply additional information based on the best available knowledge of the cropping system being modeled. Figure 4 illustrates the concept. While both experimental data (ACE) and modeler assumptions (DOME) are combined to generate model inputs for the simulation, the original field-measured data are not modified. 

DOME functions are available  to allow calculation of modeling inputs such as initial water content, initial N distribution, and other functions (see http://research.agmip.org/display/itwiki/The+DOME).

DOMEs may also be used to generate scenarios for modeling future climates, adaptation strategies, sensitivity analyses, or other hypothetical scenarios. Addition of DOME data does not alter the original dataset, and multiple DOMEs can be combined to create complex scenarios. 

See the section of this document entitled: “How to Use a DOME” for more information on the structure and content of DOME data.

## References

Kimball, B.A., J.W. White, G.W. Wall, M.J. Ottman 2016. Wheat Responses to a Wide Range of Temperatures: The Hot Serial Cereal Experiment. In: J. L. Hatfield, D. Fleisher, editors, Improving Modeling Tools to Assess Climate Change Effects on Crop Response, Adv. Agric. Syst. Model. 7. ASA, CSSA, and SSSA, Madison, WI. p. 33-44. [doi:10.2134/advagricsystmodel7.2014.0014](https://doi.org/10.2134/advagricsystmodel7.2014.0014)

Porter, C.H., C. Villalobos, D. Holzworth, R. Nelson, J.W. White, I.N. Athanasiadis, S. Janssen, D. Ripoche, J. Cufi, D. Raes, M. Zhang, R. Knapen, R. Sahajpal, K.J. Boote, J.W. Jones. 2014. Harmonization and translation of crop modeling data to ensure interoperability. Environmental Modelling and Software. 62:495-508. [doi:10.1016/j.envsoft.2014.09.004](https://doi.org/10.1016/j.envsoft.2014.09.004). 

Rosenzweig, C., J.W. Jones, J.L. Hatfield, A.C. Ruane, K.J. Boote, P. Thorburn, J.M. Antle,G.C. Nelson, C. Porter, S. Janssen, S. Asseng, B. Basso, F. Ewert, D. Wallach, G. Baigorria, and J.M. Winter.  2012. The Agricultural Model Intercomparison and Improvement Project (AgMIP): Protocols and Pilot Studies.  Ag. For. Meteor. 170:166-182[doi:10.1016/j.agrformet.2012.09.011](http://dx.doi.org/10.1016/j.agrformet.2012.09.011). 

