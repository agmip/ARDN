# How does ARDN work?

ARDN data transformations, aggregations, and translations are made possible by annotation files that allow datasets of very different formats, vocabularies, units, and physical locations to be interpreted in an automated way. ARDN tools allow data providers to create these annotations. Additional tools allow end-users of data to translate any ARDN dataset into several end-use formats for modeling and data analytics.

The ARDN data interoperability system is comprised of four interacting workflows as shown in the diagram below. In these workflows, tools (orange boxes) are used to create annotation files and AgMIP format files (blue parallelograms) from the original dataset. 

![image](https://raw.githubusercontent.com/agmip/ARDN/master/docs/images/ARDN_workflows.jpg)

The **ARDN Data Provider Tools** include [VMapper](VMapper.md), which allows a user to interactively annotate their dataset with ICASA terminology. The product of VMapper is a Sidecar File 2 (SC2). Currently data in Excel and csv formats are supported by VMapper, with a json parser in production. 

Find more information **[here]()** on the workflow for a data provider.


The **Data Tranlsation API** performs all translation functions, including conversion of a dataset to AgMIP ACEB format, translation from ACEB format to end-user formats, and extraction of a subset of data to be included in Sidecar File 3 (SC3).

**ARDN Search and Discovery Tools** are used to generate a linkage of dataset terms to ontology terms (Sidecar File 1 or SC1). SC1 provides a means for semantically aware web searches to identify datasets using specific terminology. SC3 provides the data portal (e.g., Ag Data Commons or GARDIAN) to execute advanced searches on ARDN datasets without accessing and translating the data in the archived format and location.

**ARDN Data End-User Tools** are a suite of translators which convert data from AgMIP ACEB format to various model-specific formats. These translators were originally developed by AgMIP and are maintained by the model developer teams for each model.

### Links to additional resources for data providers:
- [VMapper](VMapper.md)
- [ICASA Data Dictionary](http:/tinyurl.com/icasa-mvl)

