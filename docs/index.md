# The Agricultural Research Data Network (ARDN)

There is a major gap between the potential value of data collected in agricultural experiments and the value currently obtained through use of those data. Typically, data collected in experiments are used for the original research purpose only. Vastly greater value might be obtained if the data were combined across locations, time, and management conditions. The Agricultural Research Data Network provides tools and protocols to allow researchers to not only share their data, but to make their data interoperable and reusable. Additional tools allow end users of the data to combine and reformat ARDN data for quantitative analysis and modeling.

## Why ARDN?
The goal of ARDN is to create a distributed network for harmonized crop systems research data and to make these data available through existing data portals such as USDA's Ag Data Commons and CGIAR's GARDIAN.
For more information, see [Why ARDN?](ARDN_why.md)

## What is ARDN?
**Data Network**: ARDN is a network of datasets which can be harmonized and aggregated using a common vocabulary and format. 
**Data Interoperability Protocol**: Datasets in ARDN are connected by a common protocol for annotating data which allows the data to be interpreted in an automated way. 
More information about ARDN can be found [here](ARDN_what).

## Who are ARDN users?
ARDN **data providers** have data that they wish to make available to researchers in a format that can be interpreted in an automated way. ARDN tools assist these users to ARDN-ify their data thereby making these datasets reusable.

**End users** of ARDN data make use of the interoperability of these datasets and can download and transform the data into formats that can be used in modeling applications, data analytics, meta-analyses, and other quantitative uses.

There are several **related networks** that are compatible with ARDN protocols. ARDN has been implemented on [Ag Data Commons](https://data.nal.usda.gov/), the data and publication portal of the USDA National Agricultural Library. 
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



