# Deduplication using RecordLinkage

## Introduction

This code is designed to identify and remove duplicate records from a dataset using the RecordLinkage library in Python. The process involves comparing and matching records based on various attributes, such as names, addresses, and dates of birth.

## Setup

To run the code, make sure you have the RecordLinkage library installed. You can install it using the following command:

```bash
pip install recordlinkage
```

## Usage

1. **Loading Data:**
   - The code uses the `load_febrl4` function from the RecordLinkage library to load sample datasets (`dfA` and `dfB`).

2. **Data Preprocessing:**
   - Data is converted to uppercase for uniformity.

3. **Address Cleanup:**
   - Stop words in the address are removed, and irrelevant symbols are cleaned.

4. **Postcode Cleanup:**
   - Postcode is stripped of unnecessary characters.

5. **Indexing:**
   - The code creates index pairs using the block method for attributes like given name and date of birth. It also uses the Sorted Neighbourhood method for the social security number.

6. **Similarity Comparison:**
   - Similarity scores are calculated using the Jaro-Winkler and Levenshtein methods for various attributes like names, addresses, and dates of birth.

7. **Deduplication:**
   - Records with similarity scores above a certain threshold are considered duplicates.

## Results

The code generates a summary of the deduplication process, showing the number of record pairs with similarity scores above the threshold.

Feel free to adjust the similarity thresholds and attributes based on your specific dataset and requirements.
