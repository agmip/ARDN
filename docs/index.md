# The Agricultural Research Data Network (ARDN)

There is a major gap between the potential value of data collected in agricultural experiments and the value currently obtained through use of those data. Typically, data collected in experiments are used for the original research purpose only. Vastly greater value might be obtained if the data were combined across locations, time, and management conditions. The Agricultural Research Data Network provides tools and protocols to allow researchers to not only share their data, but to make their data interoperable and reusable. Additional tools allow end users of the data to combine and reformat ARDN data for quantitative analysis and modeling.

For more information, see [About ARDN](About_ARDN.md)


## What is ARDN?

**Data Network**: ARDN is a network of datasets which can be harmonized and aggregated using a common vocabulary and format. ARDN datasets are physically located in distributed public archives and use diverse formats, schemas, and access methods, but all ARDN datasets contain these elements:
1. Extended metadata which describe the steps needed to convert the data to AgMIP Crop Experiment (ACE) format.  More information on these metadata can be found [here](Annotation.md).
2. ARDN datasets contain information which can be described by the [ICASA vocabulary](ICASA.md).
3. ARDN datasets are collected in field crop research, variety trials, breeding trials, high throughput phenotyping experiments, long-term agro-ecological research, farm surveys, and other types of agricultural research. These data are generally associated with one or more crops, a specific location (latitude and longitude), and contain information regarding crop life cycle (e.g., planting and harvest dates), plant growth measurements (e.g., yield and yield components), crop management (e.g., fertilizer, irrigation details). The data vary widely from one experiment to another and data requirements are minimal to qualify for ARDN.
4. The ARDN interoperable data may consist of a subset of the dataset. Raw data are preserved with the original format and contents so that an interested researcher could obtain additional (non-interoperable) information. The subset of data included in ARDN is determined by the person creating the data annotation and by the variables described in the [ICASA vocabulary](ICASA.md).

**Data Interoperability Protocol**: Datasets in ARDN are connected by a common protocol for annotating data which allows the data to be interpreted in an automated way. 
1. Data annotation tools allow data providers to associate their data with ARDN. 
    - Annotation consists of three sidecar files, which are extended metadata. To read more about the ARDN sidecar files, see [ARDN dataset annotation](Annotation.md).
    - The VMapper tool assists a data provider to create ARDN sidecar file 2. To learn more, see the [VMapper documentation](VMapper.md).
2. Data translation tools allow conversion of ARDN datasets to various end user formats. See [AgMIP End-User Translation Tools](AgMIP_translators.md) for more information.

## Who are ARDN users?
ARDN users fall into two categories:
1. ARDN **data providers** have data that they wish to make available to researchers in a format that can be interpreted in an automated way. ARDN tools assist these users to ARDN-ify their data thereby making these datasets reusable.
2. **End users** of ARDN data make use of the interoperability of these datasets and can download and transform the data into formats that can be used in modeling applications, data analytics, meta-analyses, and other quantitative uses.

## Related Networks
ARDN has been implemented on [Ag Data Commons](https://data.nal.usda.gov/), the data and publication portal of the USDA National Agricultural Library. 
Compatible data interoperability standards are also being developed and implemented on the CGIAR [GARDIAN](https://gardian.bigdata.cgiar.org/#!/) platform and by the [International Fertilizer Development Center](https://ifdc.org/) (IFDC).
For more information, visit the [About ARDN](About_ARDN.md) page.

## What ARDN is NOT:
- ARDN does not (yet) include data from other agricultural domains such as livestock, pest and diseases, aquaculture, socioeconomics, and genetics. Similar methods could be developed for these domains. 
- ARDN is mainly developed for quantitative data that are used in modeling and analytics. It is less useful for categorical data, such as color, or categorical scales of damage, or other information. 
- ARDN is most useful for “legacy” data where the format and vocabulary of the dataset are not standardized. 

We hope that in the future, datasets are collected from the field using standardized vocabularies and ontologies so that the ARDN data annotation method is no longer needed. But until then, we offer these interoperability hacks!
  
## How does it work?
The ARDN data interoperability system is comprised of tools (orange boxes in diagram), and files (blue boxes). 
The tools are used to create the annotation files (Sidecar files 1, 2, and 3), the AgMIP format data file (ACEB), and the data in user-selected output formats (End User files).
A data provider uses the VMapper tool to map the variables in their data. Currently Excel and csv formats are supported by VMapper. 

![image](../images/ARDN_workflows_v2.png)

## Data user workflow diagram and description. Link to Procedures for ARDN Data End Users

## Data provider workflow diagram and description. Link to Procedures for ARDN Data Providers

For more information, see [About ARDN](About_ARDN.md)
