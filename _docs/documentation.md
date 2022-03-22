---
title: Documentation
---

<div class="col-md-8" markdown="1">

## Peekbank Framework

The Peekbank data framework consists of three components (see Figure on right): 

1. processing raw experimental datasets
2. populating a relational database
3. providing an interface to the database 

The code used to process raw datasets is hosted in <a target="_blank" href="https://github.com/langcog/peekbank-data-import" style="color:#3399f3"><code>peekbank-data-import</code></a> and processed data files are hosted on the public <a target="_blank" href="https://osf.io/pr6wu/" style="color:#3399f3">Peekbank OSF repository</a>.

The <a target="_blank" href="https://github.com/langcog/peekds" style="color:#3399f3"><code>peekds</code></a> library helps researchers convert and validate existing datasets to use the relational format of the database.

The <a target="_blank" href="https://github.com/langcog/peekbank" style="color:#3399f3"><code>peekbank</code></a> module (Python) creates a database with the relational schema and populates it with the standardized datasets produced by peekds. 
The database is implemented in MySQL, an industry standard relational database, which may be accessed by a variety of programming languages over the internet. 

The <a target="_blank" href="https://langcog.github.io/peekbankr/index.html" style="color:#3399f3"><code>peekbankr</code></a> library (R) provides an application programming interface, or API, that offers high-level abstractions for accessing data in Peekbank.

The <a target="_blank" href="https://github.com/langcog/peekbank-shiny" style="color:#3399f3"><code>peekbank-shiny</code></a> app provides a tool for interactively visualizing the data.

</div>

<div class="col-md-4" markdown="1">
<img width="360" align="right" height="540" display="block" margin-left="auto" margin-right="auto" src="../../img/peekbankflowchartv6.png">
</div>

<div class="col-md-12" markdown="1">

## Data Schema

We developed a common, tidy format for the eye-tracking data in Peekbank to ease the process of conducting cross-dataset analyses.

The schema consists of a set of tables, each tracking different types of information about a given dataset (see below for a list of tables). Each table can be accessed through functions in the <code>peekbankr</code> R package. Table columns are linked through connecting IDs (indicated by links in the schema figure below).

- **datasets**: Information about the eyetracking dataset, including citation info
- **subjects**: Data on individual participants
- **administrations**: Properties of a specific session in which an individual subject participated
- **aoi_timepoints**: Participant looking to the areas of interest (target vs. distractor) sampled at regular time intervals
- **xy_timepoints**: Gaze coordinates of participants' looking to the screen sampled at regular time intervals (if available)
- **trial_types**: Properties of each trial, including the stimuli, target location, and carrier phrase.
- **stimuli**: Stimuli in the form of word-image pairs
- **trials**: A record of the specific order in which a subject completed trials
- **aoi_region_sets**: Positional information about areas of interest (if available)

</div>

<p align="center"><img width="80%" src="../../img/schema_3.png"></p>

## Data Codebook

The codebook for individual columns in Peekbank data columns can be found in the table below (<a href="https://docs.google.com/spreadsheets/d/e/2PACX-1vR4AiOkIzIMbb2C9ksCpu6aWqYaIEiA72voek4y_05y9eY9J6XS5tLhnHZ5xnDk9LxKihicd0gN9BZY/pubhtml" target="_blank">link</a>):

<iframe src="
https://docs.google.com/spreadsheets/d/e/2PACX-1vR4AiOkIzIMbb2C9ksCpu6aWqYaIEiA72voek4y_05y9eY9J6XS5tLhnHZ5xnDk9LxKihicd0gN9BZY/pubhtml?widget=false&amp;headers=false&chrome=false" style="height: 300px; width: 100%; border: none; position:relative"></iframe> 


## Links to main repositories and tools

The Peekbank project consists of the following repositories and tools.

- Peekbank OSF repository, containing raw and standardized datasets: <a target="_blank" href="https://osf.io/pr6wu/" style="color:#3399f3">https://osf.io/pr6wu/</a>
- <code>peekbank-data-import</code>, Peekbank data import scripts: <a target="_blank" href="https://github.com/langcog/peekbank-data-import" style="color:#3399f3">https://github.com/langcog/peekbank-data-import</a>
- <code>peekds</code>, Peekbank data standard and data import functions: <a target="_blank" href="https://github.com/langcog/peekds" style="color:#3399f3">https://github.com/langcog/peekds</a>
- <code>peekbankr</code>, R package for accessing the database: <a target="_blank" href="https://github.com/langcog/peekbankr" style="color:#3399f3">https://github.com/langcog/peekbankr</a>
- <code>peekbank</code>, Peekbank database management: <a target="_blank" href="https://github.com/langcog/peekbank" style="color:#3399f3">https://github.com/langcog/peekbank</a>
- <code>peekbank-shiny</code>, interactive data visualizations using Shiny: <a target="_blank" href="https://github.com/langcog/peekbank-shiny" style="color:#3399f3">https://github.com/langcog/peekbank-shiny</a>
- <code>peekbank-website</code>, code for website frontend: <a target="_blank" href="https://github.com/langcog/peekbank-website" style="color:#3399f3">https://github.com/langcog/peekbank-website</a>

Peekbank is open source and under active development. If you run encounter a problem, please file an issue in the GitHub Issues page of the appropriate repository.

If you would like to contact us directly, email us at peekbank-dev[at]lists.stanford.edu.
