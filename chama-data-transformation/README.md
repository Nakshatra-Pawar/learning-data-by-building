# Chama Data Transformation (ETL Project)

### Built a mini ETL pipeline to transform nested JSON event data into analytics-ready tables using Python and Pandas.

## Overview

This project focuses on transforming raw event data into structured, analysis-ready datasets. The input data contains nested JSON payloads stored as strings, which require parsing and flattening before they can be used for analytics or reporting.

## Problem Statement

The input file (`case.json`) contains event records with:

* `EnqueuedTimeUtc`
* `EventName`
* `Payload` (stored as a JSON string)

Challenges involved:

* Parsing nested JSON inside a string field
* Handling multiple event types with different structures
* Flattening hierarchical data into tabular format
* Converting timestamps to a required timezone and format

## Output Tables

The pipeline generates three CSV files:

### CuratedOfferOptions.csv

* One row per option inside curated offers
* Source: `CurateOffer_Result` events
* Requires flattening nested lists (offers → options)

### DynamicPriceOption.csv

* One row per pricing option
* Source: `DynamicPrice_Result` events with provider `ApplyDynamicPricePerOption`
* `algorithmOutput` is a list → flattened into rows

### DynamicPriceRange.csv

* One row per pricing range event
* Source: `DynamicPrice_Result` events with provider `ApplyDynamicPriceRange`
* `algorithmOutput` is a dictionary → directly mapped

## Approach (ETL Pipeline)

### Extract

* Load raw JSON data using Python
* Parse the `Payload` field using `json.loads()`

### Transform

* Identify event types and providers
* Flatten nested structures into rows
* Combine data from multiple levels (event, payload, nested fields)
* Handle missing values safely using `.get()`
* Convert timestamps:

  * UTC → Brazil timezone (UTC-3)
  * Format → `DD/MM/YYYY`

### Load

* Convert processed data into Pandas DataFrames
* Export final structured datasets as CSV files

## Key Concepts Demonstrated

* JSON parsing and handling semi-structured data
* Data flattening (nested lists and dictionaries)
* Schema mapping across multiple levels
* Timezone conversion using Pandas
* Data validation and sanity checks
* Building an end-to-end ETL pipeline

## Tech Stack

* Python
* Pandas
* JSON

## Project Structure

```
chama-data-transformation/
│
├── datasets/
│   └── case.json
├── notebook.ipynb
├── CuratedOfferOptions.csv
├── DynamicPriceOption.csv
├── DynamicPriceRange.csv
└── README.md
```

## Learnings

* Working with nested and semi-structured data
* Importance of separating extraction and transformation logic
* Handling different schemas within the same dataset
* Preparing clean data for analytics and downstream use

## Future Improvements

* Modularize code into reusable functions
* Add logging and error handling
* Automate the pipeline execution
* Add schema validation checks
* Scale processing using distributed frameworks like PySpark
