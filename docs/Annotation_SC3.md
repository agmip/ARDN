# ARDN Sidecar File 3

Sidecar file 3 (SC3) contains a standard subset of the dataset which will be available on GARDIAN for advanced searches on ranges of values, simple analytics, and rapid data exploration. Because data accessible through GARDIAN are stored in different physical locations, with different formats, schemas, and vocabularies, searching through the actual datasets may not be possible within a reasonable amount of time. SC3 pre-exposes some interoperable data to enable fast querying of datasets which meet the minimum quantitative data criteria. Data contained in SC3 have already been transformed to ICASA units and variable names based on the rules in SC2, so there is no ambiguity when querying multiple datasets.

Regardless of the variables included in the dataset, only a subset of variables is included in SC3. These variables (with ICASA variable names) are listed below:
* Experimental factors (factors) 
* Crop species (crid) 
* Cultivar information (cul_text) 
* Location, decimal degrees (fl_lat and fl_long) 
* Elevation, m (flele)
* Planting date (pdate)
* Harvest date (hdate)
* Anthesis date (adat) 
* Maturity date (mdat) 
* Yield, dry matter, kg/ha (hwah)
* Aboveground biomass harvested as dry matter, kg/ha (cwah) 
* Total N fertilizer applied, kg[N]/ha (fen_tot)
* Total P fertilizer applied, kg[P]/ha (fep_tot)
* Total K fertilizer applied, kg[K]/ha ( fek_tot)
* Number of fertilizer applications (fert_#_tot)
* Total irrigation amount, mm (ir_tot)
* Number of irrigation applications (ir_#)

SC3 contains three parts: 
1. **Indexing/Metadata** – unique values of variables are stored for the subset of variables in the dataset. These are presented as key-value pairs where the key is an ICASA variable and the value is a vector including the range of unique values found in the full dataset. This allows rapid, advanced searching of data in the dataset to occur without actually accessing and interpreting the raw data. This section also contains metadata regarding the number of field observations included in the dataset, which serves as a proxy for dataset quality. This section also provides information about the weather and soils data included in the dataset. These data may be of interest to someone searching for datasets for quantitative analyses for specific purposes. These metadata include:
    1. number of treatments or rows in the columnar data – count_trtno 
    1. Number of observations of time series data:
        - Number of aboveground biomass measurements – count_biomass
        - Number of measurements of grain weight – count_grain_weight
        - Number of measurements of vegetative matter (leaf and/or stem) – count_veg_weight
        - Number of measurements of reproductive matter (pods, ears, panicle, tuber) – count_pod_weight
        - Number of LAI measurements – count_lai
        - Number of measurements of vegetative nitrogen – count_vegN
        - Number of measurements of grain N – count_grainN
        - Number of observations of pest or disease – count_pestobs
    1. Weather data: 
        - starting date – start_wdate
        - ending date  – end_wdate
    1. Soil data observations:
        - Number of soil layers for soils data (i.e., in the depth dimension) – count_soillayers
        - Number of soil moisture measurements (i.e., in the depth and time dimensions) – count_soilwat
        - Number of soil N measurements (i.e., in the depth and time dimensions) – count_soilN
<!--![image](SC3a1.png)-->
2. **Extracted data** – tab-delimited values from the dataset for the selected subset of variables. Because this is a simple table with a standard set of columnar data, it can be used directly for analytics either alone or in combination with SC3 from other datasets.
<!--![image](SC3b.png)-->
3. **Statistics** – for the selected subset of variables, summary statistics are provided, including minimum, 25th percentile, mean, median, 75th percentile, maximum, and standard deviation.
<!--![image](SC3c.png)-->


The SC3 can be generated using the information found in ACEB files, which are available after translation from an SC2 file. A post-processor has been developed to extract these data from each dataset automatically. Because the files will be auto-generated from the data, the list of variables stored in SC3 could be expanded as needed. 

SC3  provides sufficient data to enable rapid advanced searches using metadata only. This is important because datasets are distributed and may not be quickly accessed and translated.  Once a dataset is selected after a search of metadata, it can be converted to AgMIP data format using the information stored in SC2. Various model-ready formats and data analytics formats will be available to make these data useful on a variety of platforms. 

The following is a partial SC3 for the “TAMASA Ethiopia. Variety phenology calibration dataset, 2016”. The file has been shortened for brevity. The entire file may be viewed **[here](https://github.com/agmip/gardian_metadata/blob/master/TAMASA/tamasa-sc3.json)**.



[Home](index.md)

