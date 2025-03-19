# UK Food Standards Evalutation
## Overview
This project aims to evaluate food hygiene rating from the UK Food Standards Agency. The goal is to provide insights to *Eat Safe, Love* magazine helping them decide where to focus future articles. <br> *This is a fictional project that is a part of a DU Data Analytics bootcamp.*

## Table of contents
- [Overview](#overview)
- [Features](#features)
- [Instalation](#installation)
- [Analysis](#analysis)
- [Resouces/ Data Sources](#resources-data-sources)

## Features
NoSQL Setup: 
- Provides the initial set up for the database and Jupyter Notebook
- Adds in a new restaurant to the database

NoSQL Analysis:
- Exploratory analysis on the establishments collection to find which locations are best for the magazine to visit and avoid

## Installation
### Requirements
- Python 3.x
- Jupyter Notebook

### Set up
1. Install necessary libraries:
    ```bash
    pip install pymongo
    pip install pandas
    pip install pprint
    ```

2. Import the required modules:
    ```python
    from pymongo import MongoClient
    import pandas as pd
    from pprint import pprint
    ```

### Usage instructions
1. **Import the data**: 
Import the data provided in the `establishments.json` file from your Terminal. Name the database `uk_food` and the collection `establishments`.

```bash
mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json
```
2. **Finish setup**: Finish seting up the database in the Jupyter notebook `NoSQL_setup_starter.ipynb`
3. **Start analysing the data**: Proceed with analyzing the data in the Jupyter notebook `NoSQL_analysis_starter.ipynb`

## Analysis
The analysis was conducted using the `NoSQL_analysis_starter.ipynb` notebook, where specific questions posed by *Eat Safe, Love* magazine will be answered.

### Questions to Explore:
1. Which establishments have a hygiene score equal to 20?
2. Which establishments in London have a `RatingValue` greater than or equal to 4?
3. What are the top 5 establishments with a `RatingValue` of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
4. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.

### Methodology
- **Database Queries**: This project uses MongoDB queries to filter and aggregate the data in order to answer the questions.
- **Data Transformation and Visualization**: The results from the queries were converted into Pandas DataFrames to present the results clearly.

## Resources/ Data Sources
- Module 12 Challenge Files
- [UK Food Standards Agency](https://www.food.gov.uk/)
- [UK food hygiene rating data API](https://ratings.food.gov.uk/open-data/en-GB)
- I worked with my classmate Jenni Kim on this project.
- I used ChatGPT to troubleshoot code.


