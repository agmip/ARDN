# Data Provider Workflow for Ag Data Commons

The diagram below presents a typical workflow for an ARDN data provider sharing data through [Ag Data Commons (ADC)](https://data.nal.usda.gov/).

**Step 1.** A researcher wanting to ARDN-ize their data would first prepare the data for archiving on their local computer or server. If the dataset has already been archived on ADC, this step may not be necessary. However, for complex datasets, some data manipulation may be required in order to establish relational linkages within the dataset, which is a necessary element of ARDN.

- We strongly suggest the use of Tidy Data principles for preparing datasets to be used for any type of analyses. Links to tidy data paper and other useful information can be found **[here](TidyData.md)**. 

- [VMapper](VMapper.md) is used to map the variables in the dataset to the ICASA vocabulary terms. The units of the raw data are declared so that they can be converted to ICASA-compliant units at the time of translation.

- The end result of VMapper is a Sidecar 2 file or [SC2](Annotation_SC2.md), a data annotation file in JSON format. This is may not be the final version of SC2 as it does not yet contain the links to the dataset archived on Ag Data Commons. However, if the dataset being mapped has already been archived with a permanent digital object identifier (DOI) or other permanent link, then the SC2 can be finalized at this stage. 

**Step 2.**
When the dataset is prepared and annotated, it can be registered and uploaded to Ag Data Commons. A user must have a free account on Ag Data Commons. A very clear [Data Submissions Manual](https://data.nal.usda.gov/ag-data-commons-data-submission-manual) is provided to assist users in the process of creating metadata and uploading data files. The user decides when the metadata and dataset are ready for review.

**Step 3.**
The metadata goes through a curation review process and when ready, the dataset is published and a DOI is assigned (optional).


![image](https://raw.githubusercontent.com/agmip/ARDN/master/docs/images/DataProviderWorkflow_web.jpg)