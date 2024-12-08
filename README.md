### Project Goal

This project aims to identify the targets of small drug molecules using a list of PubChem IDs. To achieve this, we will access and extract relevant information from the biological test results CSV files provided by PubChem, specifically focusing on the column named "target names."

### Overall Pipeline

1. **Generate Initial Data:**
   - Create a list of PubChem IDs and their corresponding targets from the initial dataset.
   - Construct a dictionary where each PubChem ID maps to a list of its associated targets.

2. **Download Biological Test Results:**
   - Use the `pubchempy` library to download the biological test results for each PubChem ID as a CSV file.
   - After downloading, rename each file to match its corresponding PubChem ID.

3. **Extract Target Information:**
   - Parse the downloaded files to create a new dictionary.
   - In this dictionary, each key is the PubChem ID (from the file name), and the value is a list of target names extracted from the "target names" column in the CSV file.
