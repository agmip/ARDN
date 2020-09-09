# The Agricultural Research Data Network (ARDN)

There is a major gap between the potential value of data collected in agricultural experiments and the value currently obtained through use of those data. Typically, data collected in experiments are used for the original research purpose only. Vastly greater value might be obtained if the data were combined across locations, time, and management conditions. The Agricultural Research Data Network provides tools and protocols to allow researchers to not only share their data, but to make their data interoperable and reusable. Additional tools allow end users of the data to combine and reformat ARDN data for quantitative analysis and modeling.


## What is ARDN?

**Data Network**: ARDN is a network of datasets which can be harmonized and aggregated using a common vocabulary and format. ARDN datasets are physically located in distributed public archives and use diverse formats, schemas, and access methods, but all ARDN datasets contain these elements:
1.	Extended metadata which describe the steps needed to convert the data to AgMIP Crop Experiment (ACE) format.  More information on these metadata can be found here.
2.	ARDN datasets contain information which can be described by the ICASA vocabulary.
3.	ARDN datasets are collected in field crop research, variety trials, breeding trials, high throughput phenotyping experiments, long-term agro-ecological research, farm surveys, and other types of agricultural research. These data are generally associated with one or more crops, a specific location (latitude and longitude), and contain information regarding crop life cycle (e.g., planting and harvest dates), plant growth measurements (e.g., yield and yield components), crop management (e.g., fertilizer, irrigation details). The data vary widely from one experiment to another and data requirements are minimal to qualify for ARDN.
4.	The ARDN interoperable data may consist of a subset of the dataset. Raw data are preserved with the original format and contents so that an interested researcher could obtain additional (non-interoperable) information.

**Data Interoperability Protocol**: Datasets in ARDN are connected by a common protocol for annotating data which allows the data to be interpreted in an automated way. 
1.	Data annotation tools allow data providers to associate their data with ARDN. 
a.	Annotation consists of three sidecar files, which are extended metadata. To read more about the ARDN sidecar files, see ARDN data annotation.
b.	The VMapper tool assists a data provider to create ARDN sidecar file 2. To learn more, see the VMapper documentation.
2.	Data translation tools allow conversion of ARDN datasets to various end user formats.

## Who are ARDN users?
ARDN users fall into two categories:
-	ARDN data providers have data that they wish to make available to researchers in a format that can be interpreted in an automated way. ARDN tools assist these users to ARDN-ify their data thereby making these datasets reusable.
-	End users of ARDN data make use of the interoperability of these datasets and can download and transform the data into formats that can be used in modeling applications, data analytics, meta-analyses, and other quantitative uses.






You can use the [editor on GitHub](https://github.com/agmip/ARDN.github.io/edit/master/docs/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/agmip/ARDN.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
