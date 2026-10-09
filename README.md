[🇺🇸 English](README.md) | [🇧🇷 Português](README-pt.md)

# ETL in Python: Google Colab
### An Example of Using Python in an ETL Data Integration Process on Google Colab
![capa](intro.jpg)
---

## 1. Context and Objective
- This project was developed to demonstrate technical competencies in Extract, Transform, Load (ETL) data processes using Python on Google Colab. The proposal consists of integrating a municipal cartographic base from the Brazilian Institute of Geography and Statistics (IBGE) with a simulated health dataset, reproducing a common scenario of information integration from distinct sources.
- Beyond exemplifying core concepts in Data Engineering and Data Analysis, the project showcases practices in automation, data wrangling, information standardization, cross-database integration, and the generation of final outputs compatible with Business Intelligence (BI) and Geographic Information Systems (GIS) tools. The health data used is exclusively for educational purposes and was simulated to demonstrate the ETL workflow, not representing official DATASUS information.
---

## 2. Methodology
![metodologia](metodologia.jpg)
- The ETL development relied on widely used libraries in data analysis and engineering projects. Pandas was employed for tabular data manipulation and wrangling, while GeoPandas enabled the storage and processing of geospatial data. Pyogrio was used to optimize the reading of vector files from IBGE's municipal grid, and PyArrow was utilized to export the final result in the GeoParquet format.
- Additionally, the native libraries `urllib.request` and `os` were used to automate data downloads and interact with the operating system. The adopted methodology aimed to reproduce a simplified ETL workflow aligned with practices found in real-world data integration projects.
---

## 3. Performed Processes
- The process began with the automated extraction of the municipal spatial grid for the State of São Paulo provided by IBGE. After downloading and reading the vector file, a simulated health database was created containing municipal codes, municipality names, and fictional indicators for educational purposes.
- During the transformation stage, procedures for text cleaning, null value handling, data type conversion, and standardization of municipal codes (used as integration keys) were executed. Next, a merge operation was performed between the geographic base and the health database using the `merge()` function, equivalent to a LEFT JOIN in SQL.
- Finally, the integrated data was loaded into output files intended for querying, analysis, and sharing, concluding the proposed ETL workflow.
---

## 4. Results
![results](resultados.jpg)
- The project's outcome consists of a functional ETL pipeline developed in Python and executed on Google Colab. The process successfully automated the extraction of the IBGE municipal grid—featuring all 645 municipalities in the State of São Paulo—while executing the cleaning, standardization, and integration of a simulated health dataset.
- As a final product, an integrated geospatial dataset containing both geographic and tabular attributes was generated, ready for use in spatial analysis, GIS applications, and Business Intelligence tools. The project demonstrates knowledge related to tabular data manipulation, geospatial data, multi-source integration, and exporting results into formats widely adopted in the data market.
  - The notebook is available for download and is fully reproducible with all code used: [Notebook colab ETL.ipynb](ETL_em_python.ipynb)
  - The GeoParquet file containing the integrated geospatial base is available for download at: [Parquet do ETL](etl_saude_municipios_sp.parquet)
  - The tabular version for data inspection and validation is available at: [Planilha p/ Excel do ETL](etl_saude_municipios_sp.xlsx)
---

### **Thank you for reading!**
![agradecimento](encerramento.jpg)
