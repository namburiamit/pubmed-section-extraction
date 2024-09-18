# Section Extraction for Journals

## Features
- **PMID to PMCID Conversion**
- **Methods Section Extraction**
- **Transparency, Rigor, and Reproducibility Statement Extraction**
- **Multithreaded Processing**
- **Data Analysis and Visualization**

## Requirements
- Python 3.x
- Libraries:
  - os
  - requests
  - beautifulsoup4 (bs4)
  - time
  - random
  - concurrent.futures
  - tqdm
  - json
  - math
  - collections
  - statistics
  - matplotlib.pyplot

Install required libraries:
```bash
pip install requests beautifulsoup4 tqdm matplotlib
```

## 1. Journal of Neurotrauma Extraction Project

### Overview
This project extracts and analyzes the Methods and Transparency sections from articles in the *Journal of Neurotrauma*. It uses web scraping to collect data from PubMed Central (PMC) for analysis of research methodologies and transparency.