---
title: Publishing to data.govt.nz step by step
parent: Toolkit
---

_This guide will be likely be most useful to IT managers, GIS coordinators, asset managers and database admin strators._
The focus of this guide will be generic, easily uploadable datasets such as PDFs, CSVs, spreadsheets and so on.

Larger, more complex datasets, eg; geospatial will likely be unable to utilise [data.govt.nz](https://data.govt.nz) for storage and may prefer to look into their own hosting solutions.

You will still be able to index larger datasets in the data.govt.nz search engine, it's just that the resource will be located on an external service.

![Data.govt.nz homepage](http://localhost:4000/uploads/publishing-data/01-homepage.jpg)

The general process for uploading a dataset is as follows:

1. Identify datasets to publish
2. For each dataset:
  1. Export the data and ensure it is cleaned, raw data
  2. Upload the dataset to data.govt.nz, providing metadata and choosing an appropriate license
3. Schedule regular updates

## 1.0 Identify datasets to publish

For the first dataset, it's recommended that you pick something that is likely to be useful straight away. It should also be known to be of good quality as well as being free from any privacy or confidentiality issues.

Some examples of good starting datasets that don't change frequently would be **drain pipes, waste collection zones, dog walking zones, and customer service center locations**.

## 2.1 Preparing the datasets

In order to prepare data sets to maximise their usefulness, it's important to acknowledge the different types of formats available as well as the limitations that they may present:

<table>
  <thead>
    <th colspan="3">Tabular</th>
    <tr>
      <th>File type</th>
      <th>Openness</th>
      <th>Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>CSV</td>
      <td>High</td>
      <td>The best format for opening structured data (eg. As spreadsheets)</td>
    </tr>
    <tr>
      <td>XLS or XLSX</td>
      <td>Low</td>
      <td>Limits machine reading and use on non-Microsoft systems</td>
  </tbody>
  <thead>
    <th colspan="3">Spatial</th>
    <tr>
      <th>File type</th>
      <th>Openness</th>
      <th>Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>KML</td>
      <td>High</td>
      <td>An open standard developed for Google Earth. May not translate to other systems. KMZ is also available as a packaged set of KML files.</td>
    </tr>
    <tr>
      <td>WMS</td>
      <td>High</td>
      <td>Standardised format for georeferenced map images</td>
    </tr>
    <tr>
      <td>WFS</td>
      <td>High</td>
      <td>Standardised format for geographical features</td>
    </tr>
  </tbody>
  <thead>
    <th colspan="3">Text</th>
    <tr>
      <th>File type</th>
      <th>Openness</th>
      <th>Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>TXT</td>
      <td>High</td>
      <td>Simple text format readable on most operating systems. No formatting is available</td>
    </tr>
    <tr>
      <td>RTF</td>
      <td>High</td>
      <td>Simple text format readable on most operating systems which retains some formatting</td>
    </tr>
    <tr>
      <td>ODT</td>
      <td>Medium</td>
      <td>Limits machine reading</td>
    </tr>
    <tr>
      <td>DOC or DOCX</td>
      <td>Low</td>
      <td>Limits machine reading and use on non-Microsoft systems</td>
    </tr>
    <tr>
      <td>PDF</td>
      <td>Low</td>
      <td>Useful for document exchange to preserve formatting, but has limitations for machine reading, character recognition and remixing.</td>
  </tbody>
</table>

Any **tabular** data should also be cleansed. This means that files should be:

  - raw - Presented in the simplest possible format with a single header row and
  - clean - Using uniform data formatting (eg; Numerical dates, postcodes in every field) with no missing entries, no embedded non-text information, data in every field and as few mistakes as possible

**Examples of raw, clean data**
<table>
  <thead>
    <tr>
      <th>Date</th>
      <th>Age</th>
      <th>Gender</thSchedule regular updatesupdates>
      <th>Postcode</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>20/10/2013</td>
      <td>12</td>
      <td>M</td>
      <td>2580</td>
    </tr>
    <tr>
      <td>10/01/2013</td>
      <td>-</td>
      <td>F</td>
      <td>1462</td>
    </tr>
    <tr>
      <td>02/11/2011</td>
      <td>22</td>
      <td>M</td>
      <td>-</td>
    </tr>
    <tr>
      <td>12/05/2012</td>
      <td>45</td>
      <td>F</td>
      <td>1464</td>
    </tr>
    <tr>
      <td>19/01/2010</td>
      <td>75</td>
      <td>F</td>
      <td>1800</td>
    </tr>
  </tbody>
</table>

**Examples of data that is not raw or clean**

<table>
  <thead>
    <tr>
      <th colspan="4">Copyright of Dept. X</th>
    </tr>
    <tr>
      <th>Date</th>
      <th>Age</th>
      <th>Gender</th>
      <th>Postcode</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>01/20/2013</td>
      <td>Fifteen</td>
      <td>Female</td>
      <td>Barton</td>
    </tr>
    <tr>
      <td>10th Dec 11</td>
      <td>15</td>
      <td>Fem</td>
      <td>-</td>
    </tr>
    <tr>
      <td>02/11/2011</td>
      <td>xx</td>
      <td>Male</td>
      <td>3652</td>
    </tr>
    <tr>
      <td>12/05/2012</td>
      <td>45*</td>
      <td>F</td>
      <td>1464</td>
    </tr>
    <tr>
      <td>* Footnote Information</td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>

## 2.2 Creating the datasets

From the front page of the [data.govt.nz](https://data.govt.nz) website, you'll be able to see an **Add Data** button in the top right corner followed by **Submit Dataset** on the next page.

![data.govt.nz submission page](http://localhost:4000/uploads/publishing-data/02-submit.jpg)

Your submission to data.govt.nz will a few pieces of information:

  - Dataset title
  - A direct link to the dataset
  - A description of the dataset
  - The category it fits under
  - The formats it is available is
  - Re-use rights / license (**See below**)
  - Update frequency (daily, monthly, yearly?)
  - Title of the agency responsible for the dataset
  - A contact email address (which will **NOT** be published)

#### Deciding on a license

Licensing is easily the most important aspect of releasing your dataset. It will determine whether or not your dataset can be used for a commercial purpose, publically redistributed and/or whether or not others have to provide attribution for your work.

For assistance in deciding, you may wish to consult the [NZGOAL framework](https://www.ict.govt.nz/guidance-and-resources/open-government/new-zealand-government-open-access-and-licensing-nzgoal-framework/) which provides guidance for agencies to follow when releasing copyright works and non-copyright material for re-use by others.

Once you've successfully uploaded your dataset, you should be able to see it live like so in the catalogue:

![data.govt.nz dataset catalogue entry](http://localhost:4000/uploads/publishing-data/03-completed-dataset.jpg)

## 3.0 Schedule regular updates

It's important to keep a schedule of how often the datasets you have provided are updated. Some datasets may not need updating very often but others, such as weekly gas prices, will be at their peak usefulness should they be updated in a timely manner.

For the example of gas prices, it wouldn't make sense to only update the dataset once a month and interested users would likely look somewhere else for fresher data.
