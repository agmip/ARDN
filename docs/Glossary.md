# Glossary and References

**AgMIP** - [Agricultural Model Intercomparison and Improvement Project](https://agmip.org/). Much of the groundwork for ARDN was developed as part of the AgMIP Data Interoperability protocols. These protocols specify standard formats and vocabularies which were developed to facilitate ensemble modeling activities. Crop modeling groups collaborated to develop the protocols and to develop software tools for data translation to specific model formats.

Porter, C.H., C. Villalobos, D. Holzworth, R. Nelson, J.W. White, I.N. Athanasiadis, S. Janssen, D. Ripoche, J. Cufi, D. Raes, M. Zhang, R. Knapen, R. Sahajpal, K.J. Boote, J.W. Jones. 2014. Harmonization and translation of crop modeling data to ensure interoperability. Environmental Modelling and Software. 62:495-508. [doi:10.1016/j.envsoft.2014.09.004](https://doi.org/10.1016/j.envsoft.2014.09.004). 


**ARDN** - Agricultural Research Data Network


**DSSAT** - [Decision Support System for Agrotechnology Transfer](https://dssat.net/) 

Hoogenboom, G., C.H. Porter, K.J. Boote, V. Shelia, P.W. Wilkens, U. Singh, J.W. White, S. Asseng, J.I. Lizaso, L.P. Moreno, W. Pavan, R. Ogoshi, L.A. Hunt, G.Y. Tsuji, and J.W. Jones. 2019. The DSSAT crop modeling ecosystem. In: p.173-216 [K.J. Boote, editor] Advances in Crop Modeling for a Sustainable Agriculture. Burleigh Dodds Science Publishing, Cambridge, United Kingdom [doi:10.19103/AS.2019.0061.10](http://dx.doi.org/10.19103/AS.2019.0061.10)

Hoogenboom, G., C.H. Porter, V. Shelia, K.J. Boote, U. Singh, J.W. White, L.A. Hunt, R. Ogoshi, J.I. Lizaso, J. Koo, S. Asseng, A. Singels, L.P. Moreno, and J.W. Jones. 2019. Decision Support System for Agrotechnology Transfer (DSSAT) Version 4.7.5. DSSAT Foundation, Gainesville, Florida, USA.
Jones, J.W., G. Hoogenboom, C.H. Porter, K.J. Boote, W.D. Batchelor, L.A. Hunt, P.W. Wilkens, U. Singh, A.J. Gijsman, and J.T. Ritchie. 2003. DSSAT Cropping System Model. European Journal of Agronomy 18:235-265.


**ICASA** - International Consortium for Agricultural Systems Applications. ICASA developed a set of data protocols for field crop experiments. As part of these protocols, a comprehensive dictionary was created to fully describe experiments with a common vocabulary. In 2011, AgMIP adopted the ICASA Data Dictionary for use in AgMIP data interoperability protocols. The ICASA Data Dictionary (or Master Variable List) can be found **[here](http:/www.tinyurl.com/icasa-mvl)**.

White, J.W., Hunt, L.A., Boote, K.J., Jones, J.W., Koo, J., Kim, S., Porter, C.H., Wilkens, P.W., Hoogenboom, G. 2013. Integrated Description of Agricultural Field Experiments and Production: the ICASA Version 2.0 Data Standards. Computers and Electronics in Agriculture. 96:1-12.

Hunt, L.A., Hoogenboom, G., Jones, J.W., White, J.W., 2006. ICASA Version 1.0 Data Standards for Agricultural Research and Decision Support.


**Sidecar File 1** - Sidecar file 1 (SC1) contains a subset of the variables included in the dataset with corresponding ontological terms to enable semantic linkages to the dataset. This component has not been implemented in Ag Data Commons ARDN datasets but is included in the GARDIAN implementation. See ARDN data annotation for additional information.


**Sidecar File 2** - Sidecar File 2 (SC2) contains the ?roadmap? for translation of the raw data to AgMIP ACEB format. The SC2 file is in JavaScript Object Notation (JSON) format and can be generated by VMapper. The contents of an SC2 file may be reused among several datasets if the raw data schemas and vocabularies are identical. See ARDN data annotation for additional information.


**Sidecar File 3** - Sidecar file 3 (SC3) contains a subset of the dataset for a few pre-selected variables. The SC3 file contains 3 parts: a table of data extracted from the dataset, a set of unique values contained within the dataset, and a set of summary statistics for the selected variables. SC3 allows rapid searching for values of data without locating and opening the dataset, which may be in a remote location. The data table portion of SC3 allows this subset of data to be easily combined with other datasets for rapid analytics. See ARDN data annotation for additional information.



[Home](index.md)

[Site map](SiteMap.md)

