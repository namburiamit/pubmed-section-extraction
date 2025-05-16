# Section Extraction and Rigor Analysis for Neurotrauma Journals

## Project Overview
This repository supports an automated pipeline for extracting and analyzing reporting practices in two neuroscience journals:

- **Journal of Neurotrauma (JNeuro)**
- **Experimental Neurology (ExpNeuro)**

The analysis focuses on the presence of rigor and transparency criteria in published research articles, leveraging text mining and the AI-based tool **SciScore** to assess compliance with recommended scientific practices.

A natural experiment is created by comparing JNeuro (which adopted a required Rigor and Transparency section in 2023) to ExpNeuro (no such policy), across a 10-year publication span.

## Key Features
- Automated **PMID to PMCID conversion** via the NCBI ID Converter API  
- **Full-text retrieval** from PubMed Central Open Access subset (PMC-OA)  
- **HTML parsing** for structured section extraction using BeautifulSoup  
- **Identification of key sections**: Methods and (when present) Rigor & Transparency  
- **SciScore integration** for evaluating rigor criteria (e.g., randomization, blinding, RRIDs)  
- **Structured JSON output** per article for downstream analysis  
- Multithreaded processing for speed

## Requirements
- Python 3.x  
- Install libraries:
  ```bash
  pip install requests beautifulsoup4 tqdm matplotlib
  ```

### Python dependencies:
- `os`, `requests`, `bs4`, `time`, `random`, `concurrent.futures`, `tqdm`, `json`, `math`, `collections`, `statistics`, `matplotlib.pyplot`

## Repository Structure
```
pubmed-section-extraction/
├── Data/
│   ├── Extracted Experiment Set/            # JSON files of Methods sections from Experimental Neurology articles
│   ├── Extracted Jneurotrauma-new/          # JSON files of Methods sections from Journal of Neurotrauma articles
│   ├── Additional Section - extracted/      # JSON files of Rigor & Transparency sections from JNeuro (2023+)
├── final-Experimental-Neurology.ipynb       # Jupyter Notebook for ExpNeuro data extraction and SciScore analysis
├── final-JNeurotrauma.ipynb                 # Jupyter Notebook for JNeuro data extraction and SciScore analysis
├── README.md                                # Documentation and usage instructions
├── .gitignore
```

## Where is the Data?
1. **Review JSON output** in the `Data/` subfolders.


## Data and Code Availability
- **GitHub Repository**: [https://github.com/namburiamit/pubmed-section-extraction](https://github.com/namburiamit/pubmed-section-extraction)
- **Experimental Neurology JSONs**: `Data/Extracted Experiment Set`
- **JNeuro JSONs (Methods)**: `Data/Extracted Jneurotrauma-new`
- **JNeuro JSONs (Rigor Section)**: `Data/Additional Section - extracted`

---
