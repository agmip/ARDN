# What is ARDN?

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
