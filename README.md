# UK Food Standards Evaluation
**Creator**: Angelina Murdock  
**Date**: March 2025

## Overview
This project evaluates food hygiene ratings provided by the UK Food Standards Agency to assist *Eat Safe, Love* magazine in identifying establishments worthy of focus. Using **MongoDB** and **Python**, the project imports, cleans, updates, and analyzes the data to surface key insights for journalists and food critics.

## Table of contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Analysis](#analysis)
- [Resources](#resources)

## Features
**Data Setup & Cleaning**
- Loaded JSON data into MongoDB and verified with PyMongo
- Added a new restaurant and removed records
- Converted coordinates and rating values to numeric types for analysis

**Data Exploration**
- Queried by hygiene score, rating value, and location (regex and geolocation)
- Aggregated hygiene scores by Local Authority
- Output results as Pandas DataFrames for further analysis

## Installation
### Requirements
- Python 3.x
- Jupyter Notebook
- MongoDB installed and running
- pymongo, pandas, pprint

### Set up
1. **Import the data:**

    From your Terminal, run the following to import the establishments.json file into MongoDB:
    ``` bash
    mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json
    ```
2. **Setup database in Jupyter Notebook:**

    Use `NoSQL_setup.ipynb` to connect to MongoDB, verify data import, add the new restaurant, clean data types, and remove Dover records.
3. **Run analysis queries:**

    Use `NoSQL_analysis.ipynb` to explore the data, answer specific questions, and convert query results into Pandas DataFrames for reporting.

## Analysis
The analysis was conducted using the `NoSQL_analysis.ipynb` notebook and focuses on answering the following:
1. Establishments with hygiene score equal to 20
2. Establishments in London with a RatingValue ≥ 4
3. Top 5 establishments rated 5, sorted by lowest hygiene score, nearest to "Penang Flavours"
4. Number of establishments with hygiene score 0 by Local Authority (top 10) 

## Resources
- **DU Bootcamp Module 12:** Used challenge files and class materials from the bootcamp.
- **ChatGPT:** Assisted with code explanations and debugging.
- **Data Sources**:
    - [UK Food Standards Agency](https://www.food.gov.uk/)
    - [UK food hygiene rating data API](https://ratings.food.gov.uk/open-data/en-GB)



