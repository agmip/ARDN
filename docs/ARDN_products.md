# Steps to creating an ARDN Products dataset

This failed to compile. Temporarily disable content.

A data provider creates an SC2 file for the dataset that they want to include in the ARDN network. The SC2 file contains the link to the dataset, either stored on ADC or on a remote repository. A separate dataset is created on ADC to contain the SC2 and other ARDN-related data products (such as SC3, ACEB, model-ready files, etc.). The steps to create this ARDN dataset are described below. Unless stated otherwise, existing fields should not be changed.

## Step 1. Clone the metadata for the dataset being ARDN-ized. 

Click on the “Clone dataset” button at top of dataset to be cloned. Click on “Clone” again on the new screen that pops up.

## Step 2. Modify the metadata

### First block
In the **“Title”** section, remove the *“clone of”* at the beginning of the title. Keep the title and add *“: ARDN Products”* at the end.

In the **“Summary”** field, add the following text at the beginning of the summary: 

>“ARDN (Agricultural Research Data Network) annotations for `"parent dataset name"`. The ARDN project (https://data.nal.usda.gov/ardn) is a network of datasets harmonized and aggregated using the ICASA vocabulary, as recommended by USDA NAL (https://data.nal.usda.gov/data-dictionary-examples) and described in detail here:  www.tinyurl.com/icasa-mvl”. 

The remaining summary may be left from the original, or it may be modified as you prefer.


<!-- In the **“Description”** section, add the following text: 

>“ARDN provides dataset annotations which facilitate interoperability. For information on how to use ARDN annotations and other data products, see https://agmip.github.io/ARDN/ARDN_how.html.” 

The remainder of the Description should be identical to that of the original dataset.

**“Tags”** and **“Groups”** are autofillled from the cloned dataset. Leave these as-is.

**“License”** – Select CC0 (or your choice, but this should be an opensource license).

---
### “Dataset Information” block

The **“Geographic coverage”**, **“Spatial Description”**, **"Frequency”**, **“Temporal Coverage”** fields are autofilled with information from the cloned dataset. Leave these as-is.

**“Contact name”** and **“Contact email”** should be for the person who created the SC2, not necessarily the original data provider.

**“Public Access Level”** should be public.

**“Resources”** are autofilled from the cloned dataset.

---
### “Extended Metadata” block
**“Authors”** will usually be different from authors of the original dataset. Use this field to give credit to the people who generated the SC2 file and other associated ARDN product files.

**“Purpose and Methods”**
- For **“Intended Use”**, insert the following text:

>“ARDN network of interoperable data. See https://agmip.github.io/ARDN/ and https://agmip.github.io/ARDN/ARDN_how.html.”

- **“Use limitations”** – leave this the same as the original dataset.

- **“Equipment or Software Used”** – Insert the following entry:
>Ag Data Commons ARDN project page 
>https://data.nal.usda.gov/ARDN

- **“Citations”** – You can remove all citations, unless a citation exists for use of the translated data. 

- **“Funding sources”** – This would refer to funding for the SC2 generation and translation of the original data. if you generated this under the ARDN NIFA project, Select “National Institute of Food and Agriculture” from the pull-down menu and use: Award #2019-67021-29921. 

- **“Dataset DOI (digital object identifier)"** – Leave blank (ARDN datasets will not get a DOI).

- **“Product type”** – “Dataset”

- **“Cites other Datasets”** – include the name and url for the original dataset metadata record (i.e., the ADC main page for the dataset).

- **“Related Content”** – link to the original dataset here. In addition, add this link:
>Title: “ARDN website”; URL: https://agmip.github.io/ARDN/

- **“Preferred Dataset Citation”**, **"ARIS Log Number"**, **“ISO Topic(s)”**, and **“State or Territory”** – keep the same as the original dataset.

- **“Program”** – Select “ARDN” from the pull-down menu.

---
### Additional entries:
- **“Collection”** list the name of the main dataset.

- **“Highlight image”**, **“Bureau Code”**, **“Program Code”** – leave blank

- **“Publisher”** – should be autofilled as “Ag Data Commons”. 

- **“Revision information”** – can be filled when files or metadata are added, amended. This would include any automated addition of SC3, ACEB files, or model-specific files.

---
### Save the metadata

Click **“Save”**. 

When the metadata are complete and the data file(s) have been uploaded, click **“Submit for Review”**.

---
## Step 3. Add the SC2 file
From the ARDN products metadata page, click **“+ Add Resource”**, at the top of the page to upload the SC2 file.

You can browse for a file or drag it onto the "Upload" window. The name of the SC2 should match the data file name with “-sc2.json” appended. This is done automatically by VMapper and the user generally will not change this name.

Leave blank **“Data previews”**, **“Delimiter”**, and **“Embed”** fields.

In the **“Title”** field, enter: 
>"ARDN SC2 for  `parent dataset name`"

In the **“Description”** field, enter: 
>“ARDN sidecar 2 file which allows dataset to be automatically interpreted and translated to end user formats.”

For **“Format”**, select “json” from the pull-down menu

In the **“Recommended software”** field, enter:
>AgMIP / ARDN Data Factory	https://data.agmip.org/ardn/tools/data_factory 


**“Dataset”** should refer to the original dataset related to this SC2.

**“URL path settings”** – Check “Generate automatic URL alias”

---
### Save your resource file

**“Save”**

You might get a message that the resource has been added.

---
## Step 4. Procedures for generation and upload of SC3, ACEB files

 To manually upload additional files, follow instructions for adding the SC2 file as a resource to the existing dataset (step 3).

-->
