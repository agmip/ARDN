# How does ARDN work?

ARDN data transformations, aggregations, and translations are made possible by annotation files that allow datasets of very different formats, vocabularies, units, and physical locations to be interpreted in an automated way. ARDN tools allow data providers to create these annotations. Additional tools allow end-users to translate any ARDN dataset into useful formats for modeling and data analytics.

The ARDN data interoperability system is comprised of four interacting workflows as shown in the diagram below. In these workflows, tools (orange boxes) are used to create annotation files and AgMIP format files (blue parallelograms) from the original dataset. 

![image](https://raw.githubusercontent.com/agmip/ARDN/master/docs/images/ARDN_workflows.jpg)

The **ARDN Data Provider Tools** include [VMapper](VMapper.md), which allows a user to interactively annotate their dataset with ICASA terminology. The product of VMapper is a Sidecar File 2 (SC2). Currently data in Excel and csv formats are supported by VMapper, with a json parser in production. 

For more detail, see **[Workflow for Data Providers](DataProviderWorkflow.md)**.

Links to additional resources for ARDN data providers:
- [VMapper](VMapper.md)
- [ICASA Data Dictionary](http:/tinyurl.com/icasa-mvl)

**ARDN Data End-User Tools** are a suite of translators which convert data from AgMIP ACEB format to various model-specific formats. Most of these translators were originally developed by the AgMIP Data Interoperability Team and are maintained by the model developer teams for each model. The following models maintain AgMIP translators:

- [DSSAT](https://dssat.net/)
- [APSIM](https://www.apsim.info/)
- [SarraH](http://iopscience.iop.org/1748-9326/8/1/014040/article)
- [STICS](https://acsess.onlinelibrary.wiley.com/doi/abs/10.2134/advagricsystmodel2.c14)
- [WOFOST](https://www.wur.nl/en/Research-Results/Research-Institutes/Environmental-Research/Facilities-Tools/Software-models-and-databases/WOFOST.htm)
- [CropGrow-NAU](https://en.cnki.com.cn/Article_en/CJFDTotal-NYGU200701024.htm)
- [CropSyst](http://modeling.bsyse.wsu.edu/CS_Suite/cropsyst/index.html)

All of these model-specific translators have been wrapped into a desktop user interface, QuadUI, developed by AgMIP, which can be downloaded **[here](http://tools.agmip.org/quadui.php)**. 

Links to additional resources for end users of ARDN data:
- [AgMIP data tools](http://tools.agmip.org/)
- [How to use an AgMIP fomatted ACEB or JSON file](How to use an AgMIP formatted aceb or json file_v2.pdf)

The **Data Tranlsation API** performs all translation functions, including conversion of a dataset to AgMIP ACEB format, translation from ACEB format to end-user formats, and extraction of a subset of data to be included in Sidecar File 3 (SC3).

<!--For more detail, see **[Data Translation API](DataTranslationAPI.md)** -->

**ARDN Search and Discovery Tools** are used to generate a linkage of dataset terms to ontology terms (Sidecar File 1 or SC1). SC1 provides a means for semantically aware web searches to identify datasets using specific terminology. SC3 provides the data portal (e.g., Ag Data Commons or GARDIAN) to execute advanced searches on ARDN datasets without accessing and translating the data in the archived format and location.

<!-- For more detail, see **[ARDN Search and Discover Tools in ADC](SearchTools.md)** -->

