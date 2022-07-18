# VMapper

VMapper allows a user to interactively annotate their dataset and align vocabulary and units of the dataset to ICASA terminology. The original dataset is not modified by VMapper, but a [Sidecar 2 file (SC2)](Annotation_SC2.md) is generated which allows the dataset to be interpreted automatically. This process is useful for agronomic datasets that are well organized, but do not conform to any standardized vocabulary. Often these datasets have been archived and assigned a DOI (Document Object Identifier) or other persistent link. The ARDN annotation (SC2 file) allows these datasets to be interpreted, converted to AgMIP formats, combined with other datasets, and re-used for new research.

### Detailed documentation
Detailed VMapper documentation can be found **[here](https://docs.google.com/document/d/1ezs4uFWI66R-gywdKB56io1YrKVKKTvs-ynFZkebm9k/edit#heading=h.ykr4v1egu9xf)**.

### Online VMapper
VMapper is currently an online tool, available at: [data.agmip.org/ardn/tools/vmapper](https://data.agmip.org/ardn/tools/vmapper). 

#### Steps in using VMapper
1. The user selects the dataset to be mapped. This could be one or more Excel spreadsheets, comma-delimited files, or tab-delimited files. All tables in the dataset must be organized by TidyData principles: each variable is a column, each observation is a row, and each type of observational unit is a table.
1. A user may optionally select a SC2 file to work from. This may be a template developed for a similarly-structured dataset, or it may be a partially developed SC2 for the current dataset, useful if the user requires more than one session to finalize the file, or if changes are to be made.
1. The user may select the tables to be mapped, ignoring any definitions or other descriptions that do not contain mappable information.
1. For each table in the dataset, the user must define the rows which define the header data, units (optional), description (optional), the starting row for the data, and the ending row for the data (optional).
1. Each column in each table is then mapped to an ICASA variable. Built-in functions are available:
	- Units are specified as reported in the data. Unit conversion is done at translation provided that the dataset units and the ICASA units are dimensionally similar. For example lb/ac can be converted to kg/ha. 
	- The units specification allows conversions to be embedded. As an example, a soybean yield may be expressed as bushels per acre at 13% moisture, which has no direct conversion to ICASA units of kg/ha. But, assuming there are 60 bushels per pound, the units could be expressed as 60*(1-0.13)lb/acre. This specification would direct the translator to multiply each yield value by 52.2 to get units of pounds per acre of dry matter. The lb/acre can then be converted directly to kg/ha dry matter, as defined by ICASA, at translation.
	- The ICASA definitions contain codes (i.e., values in a pre-defined list) for crop species, fertilizer type, and other management categories. This prevents problems with spelling, capitalization, and punctuation. Each unique data value in a column can be mapped to an ICASA code in VMapper.
	- Excel date formats are handled automatically by the translators.
	- Fertilizer and nutrient data can be expressed as either elemental or common molecular formats. Conversions from molecular to elemental form will be handled at translation. For example, a fertilizer amount may be specified with units of P2O5 (phosphate)
1. When a dataset has been fully annotated, the template file (SC2) is saved.
	
### Ag Data Commons VMapper API
An API available through Ag Data Commons is currently under development. This API will allow ARDN data contributors to annotate their data directly through the Ag Data Commons interface.

### CGIAR Platform for Big Data API
An API available through CGLabs is currently under development. This API will allow ARDN data contributors to annotate their data directly through a CGLabs interface. The CGIAR implementation of VMapper will be extended to allow a user to choose their vocabulary for annotation, which will allow other domains to harmonize their data. 


[Home](index.md)




