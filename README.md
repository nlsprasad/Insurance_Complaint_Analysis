# Insurance Complaint Analysis

## Overview

This repository contains the analysis and exploration of insurance complaint data collected from the Texas Department of Insurance (TDI). The dataset includes detailed information on complaints filed against insurance companies, focusing on the resolution processes and factors affecting complaint handling. The goal is to uncover trends, insights, and factors that influence the timely and effective resolution of insurance complaints.

The research aims to improve customer experience by analyzing complaint types, resolution time, complaint reasons, and other factors affecting complaint resolution procedures.

## Dataset

- **Source**: [Data.gov - Insurance Complaints Data](https://catalog.data.gov/dataset/insurance-complaints-all-data)
- **Publisher**: data.austintexas.gov
- **Maintained By**: TDI ODP Administrator
- **Created On**: August 25, 2023
- **Last Updated On**: February 25, 2024
- **Total Instances**: 246,243
- **Features**: 17
- **Data Description**: The dataset includes various attributes related to insurance complaints, such as:
  - Complaint Number
  - Complaint Filed Against (company/agent)
  - Complaint Filed By (complainant)
  - Reason Complaint Filed
  - Confirmed Complaint (Yes/No)
  - Complaint Type
  - Coverage Type
  - Resolution Time (difference between Received Date and Closed Date)
  - Respondent Role
  - Methods of Resolution (e.g., Settlement, Denial, etc.)

## Research Questions

- What are the primary factors influencing complaint resolution, and how do variables like complaint type, coverage type, and respondent role impact resolution outcomes?
- How have insurance complaints evolved over time, considering seasonal trends, variations in complaint frequency, and changes in complaint types?
- What are the key factors contributing to effective complaint handling procedures, including response time variations, resolution rates, and best practices?

## Analysis Methods

The analysis involves a combination of the following methods:

- **Text Mining**: To extract patterns from unstructured complaint data.
- **Natural Language Processing (NLP)**: To uncover sentiment and quality aspects of complaints.
- **Clustering**: To group similar complaints and identify patterns in complaint handling.
- **Exploratory Data Analysis (EDA)**: To investigate seasonal trends, complaint types, and the relationship between variables.
  
### Key EDA Questions

- How do reasons for filing complaints differ between confirmed and unconfirmed complaints?
- What is the average time taken to resolve a complaint?
- What proportion of complaints are resolved compared to those that remain unresolved?

## Potential Issues and Solutions

- **Missing Data**: Some columns, like the Keywords column, have a significant amount of missing values. We plan to impute missing values using the mode and split multi-keyword rows into separate columns.
- **Inconsistent Data**: There are inconsistent date formats (DD/MM/YYYY vs YYYY-MM-DD). We'll standardize date formats using Python's `datetime` package.
- **Data Volume**: The dataset is large, which may pose challenges for analysis. We will employ data cleaning techniques like error correction, standardization, and manipulation to handle large volumes efficiently.

## Installation

To get started with this project, you'll need to install the required Python packages:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn nltk
