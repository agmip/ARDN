# How does ARDN work?

The ARDN data interoperability system is comprised of four interacting workflows as shown in the diagram below. Tools (orange boxes) are used to create and files (blue parallelograms) from the user-supplied datasets and from other ARDN files previously generated. 

The "Data Provider Tools" include VMapper, which allows a user to interactively annotate their dataset with ICASA terminology. The product of VMapper is a Sidecar File 2 (SC2). Currently Excel and csv formats are supported by VMapper, with a json parser in production.

The "Data Tranlsation API" performs all translation functions, including conversion of a dataset to AgMIP ACEB format, translation from ACEB format to end-user formats, and extraction of a subset of data to be included in Sidecar File 3 (SC3).

"ARDN Search and Discovery Tools" are used to generate a linkage of dataset terms to ontology terms (Sidecar File 1 or SC1). SC1 provides a means for semantically aware web searches to identify datasets using specific terminology. SC3 provides the data portal (e.g., Ag Data Commons or GARDIAN) to execute advanced searches on ARDN datasets without accessing and translating the data in the archived format and location.

"ARDN Data End-User Tools" are a suite of translators which convert data from AgMIP ACEB format to various model-specific formats. These translators were originally developed by AgMIP and are maintained by the model developer teams for each model.

![image](https://raw.githubusercontent.com/agmip/ARDN/master/docs/images//AgMIP_workflows.jpg)
<!-- Comment ![image]/images/AgMIP_workflows.jpg)-->
