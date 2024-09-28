<h1>ARERA - Energy Offers</h1>
<h2>Data Collection Through Web Scraping</h2>

This repository contains a Jupyter notebook that extracts energy offers from the ARERA (Autorità di Regolazione per Energia Reti e Ambiente) website. The data is collected through automated web scraping from the [Il Portale Offerte](https://www.ilportaleofferte.it/portaleOfferte/it/confronto-tariffe-prezzi-luce-gas.page) website, which provides comprehensive information on electricity pricing and offers in Italy. Users can customize their data extraction by specifying the postal codes (CAP) of interest, simply by adjusting the relevant parameters within the code.

The code is designed to scrape detailed information about electricity offers for specific municipalities. It retrieves various attributes such as the offer name, validity dates, annual costs, and pricing components, focusing on user-friendly and accessible information.

The code functions by initiating a web browser session using `Selenium`, which simulates user interaction with the webpage. It uses `WebDriverWait` to ensure elements are loaded before performing actions like clicking and selecting options from dropdowns. Relevant data is extracted from the HTML structure using XPath and CSS selectors, and the scraped information is stored in a structured list.

After collecting the data for each municipality, the notebook compiles the results into a pandas DataFrame, handling necessary conversions for numeric and date formats. This organized data format makes it straightforward to analyze trends in energy pricing and offers over time.

This code was developed during an internship at [**ASTAT**](https://astat.provincia.bz.it/it/default.asp) (Provincial Institute of Statistics of Bolzano) with the main goal to facilitate the extraction of energy offer data, which can serve as a valuable resource for further analysis and monitoring of commodities prices in South Tyrol. 

## Repository Structure

```
├── ARERA_OfferteEnergia.ipynb                 # Main Jupyter notebook containing the data extraction code
├── results/                                   # Directory for example output files generated from the data extraction
│   ├── ARERA_EnergiaElettrica-2024-09-26.xlsx                  # Extracted data for energy offers dated September 26, 2024
│   ├── ARERA_EnergiaElettrica-2024-09-27.xlsx                  # Extracted data for energy offers dated September 27, 2024
│   └── ARERA_EnergiaElettrica-39100-Bolzano-2024-09-26.xlsx    # Extracted data for energy offers specific to Bolzano, dated September 26, 2024
├── requirements.txt                           # Dependencies for the project (used to recreate the environment)
└── README.md                                  # Project README file providing an overview and instructions

```

## Key Files

- **ARERA_OfferteEnergia.ipynb**: The primary Jupyter notebook that includes the code for extracting energy offer data from the ARERA website.
- **results/**: Directory containing output files generated by the data extraction process, showcasing the results for different dates and locations.
- **requirements.txt:** A text file listing the Python dependencies needed to run the project, useful for recreating the environment and ensuring compatibility.

## How to Run

**1. Clone the repository**
```
git clone https://github.com/artessari/WebScraping_EnergyOffers
cd WebScraping_EnergyOffers
```

**2. Install Dependencies**

To install the required Python libraries, run:
```
pip install -r requirements.txt
```

**3. Run Jupyter Notebook**

To explore the project interactively, launch the notebook.

### References

**ARERA** - Autorità di Regolazione per Energia Reti e Ambiente (Regulatory Authority for Energy, Networks and Environment)

Source for Web Scraping: [Il Portale Offerte](https://www.ilportaleofferte.it/portaleOfferte/it/confronto-tariffe-prezzi-luce-gas.page)
