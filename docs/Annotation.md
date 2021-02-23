# Dataset Annotation

ARDN dataset annotation acts as extended metadata, accessible in a centralized repository. ARDN dataset annotation consists of three “sidecar files” which contain information to allow automated interpretation of the dataset contents. Generation of these annotation “sidecar files” is the first step toward the goal of making ARDN datasets interoperable for use in models, data analytics, and other quantitative processes. 

All three sidecar files are formatted using JavaScript Object Notation (JSON). The intent and content of each file are described below, with links to more detailed descriptions. 

## Sidecar file #1 (SC1) 

**Note: SC1 has NOT been implemented for the ARDN network in Ag Data Commons but is an important component of the ARDN network in GARDIAN.**

SC1 provides a map of column data headers to ontology terms from Agronomy Ontology, Units Ontology, Crop Ontology, Trait Ontology, Environment Ontology, and other ontologies as needed. These mappings allow semantic linkage for all qualifying datasets. Quantitative data must be mapped to at least two ontological terms: at least one that describes the data and at least one that describes the units of measurement. An example of how a grain yield term could be represented in JSON format is shown below:


                {
                "column_index": 22,
                "terms": [
                  {
                    "term_url": "http://purl.obolibrary.org/obo/TO_0000396"
                  }
                ], 
                "unit_url": "http://purl.obolibrary.org/obo/UO_0000283"
              },

where "column_index": 22 refers to the header for the column of data containing maize grain yield, "http://purl.obolibrary.org/obo/TO_0000396" is the uri  for the corresponding term in the trait ontology, and "http://purl.obolibrary.org/obo/UO_0000283" is the uri corresponding term in the Units Ontology. 

In addition to variable mapping, SC1 files contain metadata that describe who generated the dataset annotation, the source location of the raw data, the content of the file, and where data are located in the file. 

A more detailed description of SC1 can be found **[here](Annotation_SC1.md)**.

## Sidecar file #2 (SC2) 

SC2 contains the “roadmap” for translation of the raw dataset into AgMIP ACEB format. This includes instructions for accessing the file(s), locating relevant ARDN data within the file, associating the variables with ICASA vocabulary, and defining the units of the data. The data provider may specify values of data which are not explicitly contained within the dataset. For example, a maize study may not contain any information in the dataset itself that the crop is maize. However, for that information to be included in the ARDN data, it must be explicitly stated. Other functions allow transformations of the data to describe the equivalent ICASA variable. For example, planting density may be calculated from row spacing and plant spacing within a row. That calculation can be specified in SC2.

An example of a simple definition is shown in the following JSON snippet:


              {
                "icasa": "hwam",
                "column_index": 22,
                "unit": "kg/ha"
              },

where "hwam" is the ICASA term for harvested yield at maturity in kg/ha, "column_index": 22 indicates the location of the column of data,  and "unit": "kg/ha" indicates the units for the term in the raw data. The translator has logic to automatically convert units as necessary to ICASA-compliant units using a unit conversion library based on [UDUNITS](https://www.unidata.ucar.edu/software/udunits/udunits-2-units.html).

In this simple case, the example for harvested grain weight is not much different than the SC1 snippet for this variable. But more complex transformations can be expressed. In the snippet below, planting density ("plpop") is computed from the spacing between rows ("plrs") and spacing of plants within a row ("plsp"). The formula, "10^4/(plrs * plsp)" , includes a conversion factor from cm-2 to m-2.    

    {
      "icasa": "plpop",
      "formula": "10^4/(plrs * plsp)",
      "unit": "m-2"
    },


A tool (VMapper) has been developed at UF to assist a user in mapping variables in Excel spreadsheets or CSV (comma-separated values) files to ICASA vocabulary; to specify the units of each variable; and to specify relational links between data in multiple sheets (if applicable). With this information, the app can then write the SC2 in JSON format. 

A more detailed description of SC2 can be found **[here](Annotation_SC2.md)**.

## Sidecar file #3 (SC3) 

SC3 contains data which will be available on ARDN data portals (e.g., Ag Data Commons and GARDIAN) to facilitate rapid, complex searches and basic analytics. Because the actual datasets in ARDN networks are stored in different physical locations, with different formats, schemas, and vocabularies, searching through the actual datasets may not be possible within a reasonable amount of time. SC3 pre-exposes some interoperable data to enable fast querying of ARDN datasets.

The variables or keys included in SC3 are (with ICASA variable names):
-	Experimental factors (factors)
-	Crop species (crid)
-	Cultivar information (cul_text)
-	Location (fl_lat and  fl_long)
-	Elevation (flele)
-	Planting date (pdate)
-	Harvest date (hdate)
-	Anthesis date (adat) 
-	Maturity date (mdat)
-	Yield, dry matter (hwah)
-	Aboveground biomass harvested as dry matter (cwah) 
-	Total N fertilizer applied (fen_tot)
-	Total P fertilizer applied (fep_tot)
-	Total K fertilizer applied (fek_tot)
-	number of fertilizer applications (fert_#_tot)
-	Total irrigation amount (mm) (ir_tot)
-	number of irrigation applications (ir_#)

SC3 contains three parts. The first part, SC3a, contains data extracted from the raw dataset which can be used for indexing, allowing rapid, advanced searches of annotated datasets. SC3a is a list of unique values of the variables of interest, presented as key-value pairs where the key is an ICASA variable name and the value is a vector including the range of unique values found in the full dataset. Additional metadata are included in SC3a which describe the number of treatments, the number of measurements of key variables, and the amount of weather and soil data included in the dataset. These data may be of interest to someone searching for datasets for quantitative analyses for specific purposes. 

The second part of SC3 contains a subset of the dataset, which are stored in tab-delimited format. Because this is a simple table with a standard set of columnar data, it can be used directly for analytics either alone or in combination with SC3 from other datasets.

The third section of SC3 contains statistics for the selected set of variables, including minimum, 25th percentile, mean, median, 75th percentile, maximum, and standard deviation. 

All three sections of SC3 can be generated using the information found in any AgMIP Crop Experiment Binary (ACEB) file. As part of the translation process, the SC3 data is extracted from each dataset automatically after translation. Because the files will be automatically generated from the data, the list of variables stored in SC3 could be expanded as needed. However, if the list of SC3 variables is expanded, older datasets would need to be reprocessed. 

SC3 also provides sufficient data to enable rapid advanced searches using metadata only. This is important because datasets are distributed and may not be quickly accessed and translated. Once a dataset is selected after a search of metadata, it can be converted to AgMIP data format using the information stored in SC2. Various model-ready formats and data analytics formats will be available to make these data useful on a variety of platforms. 

A more detailed description of SC3 can be found **[here](Annotation_SC3.md)**.
