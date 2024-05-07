# Patient Data Processor

## Overview
This Python script serves as a tool for processing patient data from the MIMIC-IV dataset to generate automated discharge summaries. It involves loading and transforming data, creating a multi-leveled dataframe, retrieving relevant information, and generating discharge summaries using advanced AI models.

## Dependencies
- pandas
- numpy
- json
- icd_conversion
- torch
- transformers

## Usage
```python
from patient_data_processor import PatientDataProcessor

# Initialize the processor with subject_id and hadm_id
processor = PatientDataProcessor(subject_id, hadm_id)

# Process the data and generate discharge summary
discharge_summary = processor.process_data()

print(discharge_summary)
```

## Installation
1. Clone the repository: git clone https://github.com/ColdSeal/DH_602_BioStat_Boosters.git
2. Install required dependencies: pip install pandas numpy torch transformers

## Usage
```python
from patient_data_processor import PatientDataProcessor

# Initialize PatientDataProcessor with subject_id and hadm_id
processor = PatientDataProcessor(subject_id, hadm_id)

# Process patient data and generate discharge summary
discharge_summary = processor.process_data()
```

## How It Works
1. Data Loading and Transformation: The script loads necessary CSV files from the MIMIC-IV dataset and transforms datetime columns to Datetime format for consistency.
2. Data Processing: It processes patient data, creates a main dataframe containing relevant information, and categorizes data based on discharge summary categories.
3. Text Generation: Utilizing a transformer-based language model, the script generates coherent summaries for each discharge summary category by converting tabular data into textual paragraphs.
4. Template Generation: Finally, it consolidates the generated summaries into a structured discharge summary template.

## Example
```python
from patient_data_processor import PatientDataProcessor

# Initialize PatientDataProcessor with subject_id and hadm_id
processor = PatientDataProcessor("subject_id_value", "hadm_id_value")

# Process patient data and generate discharge summary
discharge_summary = processor.process_data()
print(discharge_summary)
```
