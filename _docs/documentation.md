---
title: Documentation
---

## Peekbank Framework

<img align="right" width="360" height="540" src="../../img/peekbankflowchartv6.png">

The Peekbank data framework consists of three components (see Figure on right): 

1. processing raw experimental datasets
2. populating a relational database
3. providing an interface to the database

The <code>peekds</code> library helps researchers convert and validate existing datasets to use the relational format of the database. 

The <code>peekbank</code> module (Python) creates a database with the relational schema and populates it with the standardized datasets produced by peekds. 
The database is implemented in MySQL, an industry standard relational database, which may be accessed by a variety of programming languages over the internet. 

The <code>peekbankr</code> library (R) provides an application programming interface, or API, that offers high-level abstractions for accessing data in Peekbank.

## Data Schema



## Data Codebook


## Links to repositories and tools

The Peekbank project consists of the following repositories and tools.

- Peekbank repository with raw and standardized datasets: [https://osf.io/pr6wu/](https://osf.io/pr6wu/)
- Peekbank data import scripts: [http://github.com/langcog/peekbank-data-import](http://github.com/langcog/peekbank-data-import)
- Peek data standard and data import functions: [http://github.com/langcog/peekds](http://github.com/langcog/peekds)
- R package for Accessing the database: [http://github.com/langcog/peekds](https://github.com/langcog/peekbankr/)
- Peekbank database management: [http://github.com/langcog/peekds](http://github.com/langcog/peekbank)
- Interactive data visualizations using Shiny: [http://github.com/langcog/peekbank-shiny](http://github.com/langcog/peekbank-shiny)
- Website frontend: [http://github.com/langcog/peekbank-website](http://github.com/langcog/peekbank-website)


