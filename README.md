# MarineSpeciesModeller

## Introducuction
MarineSpeciesModeller is an open-source, standardized pipeline specifically designed for modelling marine species distributions using publicly available biodiversity and environmental datasets. By integrating taxonomic validation from the [World Register of Marine Species (WoRMS)](https://www.marinespecies.org/index.php), marine biodiversity observations from the [Global Biodiversity Information Facility (GBIF)](https://www.gbif.org), and environmental data provided by [Copernicus Marine](https://marine.copernicus.eu/), this pipeline addresses key challenges faced in marine biodiversity modelling.

Unique Selling Points:

* **Scalable File Storage:** The pipeline employs scalable data formats (netCDF and parquet files), enabling efficient handling and processing of very large marine biodiversity and environmental datasets.

* **Target Group Background Approach:** Specifically adapted to marine datasets, this methodology significantly reduces sampling bias by selecting background samples from datasets that share similar systematic biases as species observations.

* **Precise Monthly Data Matching:** Observations are matched with environmental data corresponding precisely to the month of observation. This accounts for the highly dynamic marine environment and the migratory behaviors of marine species, improving model accuracy and reliability.

MarineSpeciesModeller facilitates accurate predictions of marine biodiversity shifts and species migration patterns, providing valuable insights to support conservation planning, ecosystem management, and policymaking. The pipeline is designed to be scalable and adaptable, supporting future expansions including the integration of additional datasets and advanced machine learning methods.

## Setup
The pipeline currently exists as an `Rmarkdown` script including some python code. To get started, follow [these instructions](https://rpubs.com/dehbanh_91/Rpython) for R, Rstudio, and Python setup, then install all the required packages with `$pip install` (or your favourite package manager) for python and `install.packages()` for R. Once that is done you should be ready to run the markdown just like any notebook.

## Code
We follow the `tidyverse` style guide for R and `PEP8` for Python. For bugs and feedback, please submit an issue on our [GitHub repository](https://github.com/OceanOS-MVP/marine_sdm).

## Originality
This code base was created as part of the "Hack for a Liveable Planet - Biodiversity Hackathon". We use a number of open-source libraries, all of which are clearly discernible from the way they are loaded in the code.

## Scalability
We use big data technology (`parquet` files, `netCDF`) to help users manage even large datasets on resource constrained local environments.
Please note that some operations, such as the WORMS programmatic download, can take a long time. It might be worth contacting [WORMS](https://www.marinespecies.org/about.php) directly for a copy of the database instead.

## Known limitations and future work
Potential areas for further development:
* Modularize workflow from current linear markdown flow to utility functions grouped by topics
* Migrate code to an R package
* Add unit tests
