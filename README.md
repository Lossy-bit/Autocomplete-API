# Extracting Names from Autocomplete-API

## Project Overview
This project explores an undocumented autocomplete API to extract all possible names from the system. The API exists in three versions: v1, v2, and v3. Each version was analyzed, and a solution was developed to handle the API's constraints efficiently.

## Repository Contents
- **Notebooks**
  - `v1.ipynb`: Extracts names using the v1 endpoint.
  - `v2.ipynb`: Extracts names using the v2 endpoint.
  - `v3.ipynb`: Extracts names using the v3 endpoint.

- **Output Files**
  - `output_v1.txt`: Extracted names from v1.
  - `output_v2.txt`: Extracted names from v2.
  - `output_v3.txt`: Extracted names from v3.

## How to Run
1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd Extracting-Names-from-Autocomplete-API
   ```

2. Open and run the notebooks:
   - Launch Jupyter Notebook:
     ```bash
     jupyter notebook
     ```
   - Open each notebook (`v1.ipynb`, `v2.ipynb`, `v3.ipynb`) and run all cells.

Alternatively, you can directly access the output files without running the notebooks.

## Approach and Findings
### 1. API Exploration
- Started by probing the `/v1/autocomplete?query=<string>` endpoint.
- Discovered that partial queries return progressively more suggestions.
- Implemented a systematic query generation strategy to uncover all available names.

### 2. Handling Constraints
- **Rate Limiting:** Introduced automatic retries with exponential backoff on HTTP 429 errors.
- **Response Behavior:** Detected varying behaviors between v1, v2, and v3 (e.g., different response structures and limits per request).

## Results
- **Total requests made:** v1: 12,897; v2: 3,108; v3: 2,602
- **Total names extracted:** v1: 18,632; v2: 13,730; v3: 12,517


---
Happy extracting!


