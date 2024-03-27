# Data on COVID-19 (coronavirus) by _Our World in Data_
> copy (and reduced) ver for lab
[Source](https://github.com/owid/covid-19-data/tree/master/public/data)
Our complete COVID-19 dataset is a collection of the COVID-19 data maintained by [_Our World in Data_](https://ourworldindata.org/coronavirus). We will update it daily throughout the duration of the COVID-19 pandemic (more information on our updating process and schedule [here](https://docs.owid.io/projects/covid/en/latest/data-pipeline.html#overview)). It includes the following data:

| Metrics                     | Source                                                    | Updated | Countries |
|-----------------------------|-----------------------------------------------------------|---------|-----------|
| Vaccinations                | Official data collated by the Our World in Data team      | Daily   | 218       |
| Tests & positivity          | Official data collated by the Our World in Data team      | No longer updated (read more: https://github.com/owid/covid-19-data/discussions/2667)  | 193       |
| Hospital & ICU              | Official data collated by the Our World in Data team      | Daily   | 46        |
| Confirmed cases             | WHO COVID-19 Data                                    | Daily   | 219        |
| Confirmed deaths            | WHO COVID-19 Data                                    | Daily   | 219       |
| Reproduction rate           | Arroyo-Marioli F, Bullano F, Kucinskas S, Rondón-Moreno C | Daily   | 196        |
| Policy responses            | Oxford COVID-19 Government Response Tracker               | Daily   | 185        |
| Other variables of interest | International organizations (UN, World Bank, OECD, IHME…) | Fixed   | 242       |

A [specific section of this repository](https://github.com/owid/covid-19-data/tree/master/public/data/vaccinations) is also dedicated to **vaccinations**, with a lighter dataset containing only vaccination data.


## The data you find here and our data sources

- **Confirmed cases and deaths:** this data is collected from the [World Health Organization Coronavirus Dashboard](https://covid19.who.int/data). The cases & deaths dataset is updated daily.
  - Note 1: Time/date stamps reflect when the data was last updated by WHO. Due to the time required to process and validate the incoming data, there is a delay between reporting to WHO and the update of the dashboard.
  - Note 2: Counts and corrections made after these times will be carried forward to the next reporting cycle for that specific region. Delayed reporting for any specific country, territory or area may result in pooled counts for multiple days being presented, with a retrospective update to counts on previous days to accurately reflect trends. Significant data errors detected or reported to WHO may be corrected at more frequent intervals.
- **Hospitalizations and intensive care unit (ICU) admissions:** our data is collected from official sources and collated by Our World in Data. The complete list of country-by-country sources is available [here](https://github.com/owid/covid-19-data/blob/master/public/data/hospitalizations/locations.csv).
- **Testing for COVID-19:** this data is collected by the _Our World in Data_ team from official reports; you can find
further details in our post on COVID-19 testing, including our [checklist of questions to understand testing
data](https://ourworldindata.org/coronavirus-testing#our-checklist-for-covid-19-testing-data), information on
[geographical and temporal
coverage](https://ourworldindata.org/coronavirus-testing#which-countries-do-we-have-testing-data-for), and [detailed
country-by-country source information](https://ourworldindata.org/coronavirus-testing#source-information-country-by-country). **On 23 June 2022, we stopped adding new datapoints to our COVID-19 testing dataset.** You can read more [here](https://github.com/owid/covid-19-data/discussions/2667).
- **Vaccinations against COVID-19:** this data is collected by the _Our World in Data_ team from official reports.
- **Other variables:** this data is collected from a variety of sources (United Nations, World Bank, Global Burden of Disease, Blavatnik School of Government, etc.). More information is available in [our codebook](https://github.com/owid/covid-19-data/tree/master/public/data/owid-covid-codebook.csv).


## The complete _Our World in Data_ COVID-19 dataset

**Our complete COVID-19 dataset is available in [CSV](https://covid.ourworldindata.org/data/owid-covid-data.csv), [XLSX](https://covid.ourworldindata.org/data/owid-covid-data.xlsx), and [JSON](https://covid.ourworldindata.org/data/owid-covid-data.json) formats, and includes all of our historical data on the pandemic up to the date of publication.**

The CSV and XLSX files follow a format of 1 row per location and date. The JSON version is split by country ISO code, with static variables and an array of daily records.

The variables represent all of our main data related to confirmed cases, deaths, hospitalizations, and testing, as well as other variables of potential interest.

### Confirmed cases

| Variable                         | Description                                                                                                                                                                                            |
|:---------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `total_cases`                    | Total confirmed cases of COVID-19. Counts can include probable cases, where reported.                                                                                                                  |
| `new_cases`                      | New confirmed cases of COVID-19. Counts can include probable cases, where reported. In rare cases where our source reports a negative daily change due to a data correction, we set this metric to NA. |
| `total_cases_per_million`        | Total confirmed cases of COVID-19 per 1,000,000 people. Counts can include probable cases, where reported.                                                                                             |
| `new_cases_per_million`          | New confirmed cases of COVID-19 per 1,000,000 people. Counts can include probable cases, where reported.                                                                                               |                                                                              |

### Confirmed deaths

| Variable                          | Description                                                                                                                                                                                               |
|:----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `total_deaths`                    | Total deaths attributed to COVID-19. Counts can include probable deaths, where reported.                                                                                                                  |
| `new_deaths`                      | New deaths attributed to COVID-19. Counts can include probable deaths, where reported. In rare cases where our source reports a negative daily change due to a data correction, we set this metric to NA. |
| `total_deaths_per_million`        | Total deaths attributed to COVID-19 per 1,000,000 people. Counts can include probable deaths, where reported.                                                                                             |
| `new_deaths_per_million`          | New deaths attributed to COVID-19 per 1,000,000 people. Counts can include probable deaths, where reported.                                                                                               |

#### Notes:
* Due to varying protocols and challenges in the attribution of the cause of death, the number of confirmed deaths may not accurately represent the true number of deaths caused by COVID-19.

### Policy responses

| Variable           | Description                                                                                                                                                                                                         |
|:-------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stringency_index` | Government Response Stringency Index: composite measure based on 9 response indicators including school closures, workplace closures, and travel bans, rescaled to a value from 0 to 100 (100 = strictest response) |


### Tests & positivity
On 23 June 2022, we stopped adding new datapoints to our COVID-19 testing dataset. You can read more at https://github.com/owid/covid-19-data/discussions/2667.
| Variable                          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `total_tests`                     | Total tests for COVID-19                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| `new_tests`                       | New tests for COVID-19 (only calculated for consecutive days)                                                                                                                                                                                                                                                                                                                                                                                                         |
| `total_tests_per_thousand`        | Total tests for COVID-19 per 1,000 people                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `new_tests_per_thousand`          | New tests for COVID-19 per 1,000 people                                                                                                                                                                                                                                                                                                                                                                                                                               |
| `positive_rate`                   | The share of COVID-19 tests that are positive, given as a rolling 7-day average (this is the inverse of tests_per_case)                                                                                                                                                                                                                                                                                                                                               |
| `tests_per_case`                  | Tests conducted per new confirmed case of COVID-19, given as a rolling 7-day average (this is the inverse of positive_rate)                                                                                                                                                                                                                                                                                                                                           |

### Vaccinations

| Variable                                     | Description                                                                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `total_vaccinations`                         | Total number of COVID-19 vaccination doses administered                                                                                                                                                                                                                                                                                           |
| `people_vaccinated`                          | Total number of people who received at least one vaccine dose                                                                                                                                                                                                                                                                                     |
| `people_fully_vaccinated`                    | Total number of people who received all doses prescribed by the initial vaccination protocol                                                                                                                                                                                                                                                      |
| `total_boosters`                             | Total number of COVID-19 vaccination booster doses administered (doses administered beyond the number prescribed by the vaccination protocol)                                                                                                                                                                                                     |
| `new_vaccinations`                           | New COVID-19 vaccination doses administered (only calculated for consecutive days)                                                                                                                                                                                                                                                                |
| `total_vaccinations_per_hundred`             | Total number of COVID-19 vaccination doses administered per 100 people in the total population                                                                                                                                                                                                                                                    |
| `people_vaccinated_per_hundred`              | Total number of people who received at least one vaccine dose per 100 people in the total population                                                                                                                                                                                                                                              |
| `people_fully_vaccinated_per_hundred`        | Total number of people who received all doses prescribed by the initial vaccination protocol per 100 people in the total population                                                                                                                                                                                                               |
| `total_boosters_per_hundred`                 | Total number of COVID-19 vaccination booster doses administered per 100 people in the total population                                                                                                                                                                                                                                            |

### Others

| Variable                     | Description                                                                                                                                                                                                                                |
|:-----------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `iso_code`                   | ISO 3166-1 alpha-3 – three-letter country codes. Note that OWID-defined regions (e.g. continents like 'Europe') contain prefix 'OWID_'.                                                                                                    |
| `continent`                  | Continent of the geographical location                                                                                                                                                                                                     |
| `location`                   | Geographical location                                                                                                                                                                                                                      |
| `date`                       | Date of observation                                                                                                                                                                                                                        |
| `population`                 | Population (latest available values). See https://github.com/owid/covid-19-data/blob/master/scripts/input/un/population_latest.csv for full list of sources                                                                                |
| `population_density`         | Number of people divided by land area, measured in square kilometers, most recent year available                                                                                                                                           |
| `median_age`                 | Median age of the population, UN projection for 2020                                                                                                                                                                                       |
| `aged_65_older`              | Share of the population that is 65 years and older, most recent year available                                                                                                                                                             |
| `aged_70_older`              | Share of the population that is 70 years and older in 2015                                                                                                                                                                                 |
| `cardiovasc_death_rate`      | Death rate from cardiovascular disease in 2017 (annual number of deaths per 100,000 people)                                                                                                                                                |
| `diabetes_prevalence`        | Diabetes prevalence (% of population aged 20 to 79) in 2017                                                                                                                                                                                |
| `female_smokers`             | Share of women who smoke, most recent year available                                                                                                                                                                                       |
| `male_smokers`               | Share of men who smoke, most recent year available                                                                                                                                                                                         |

## Additional files and information

If you are interested in the individual files that make up the complete dataset, or more detailed information, other files can be found in the subfolders:

- [`latest`](https://github.com/owid/covid-19-data/tree/master/public/data/latest): shortened version of our complete dataset with only the latest value for each location and metric (within a limit of 2 weeks in the past). This file is available in CSV, XLSX, and JSON formats.
- [`cases_death`](https://github.com/owid/covid-19-data/tree/master/public/data/cases_death): data from the COVID-19 dashboard by the WHO, related to confirmed cases and deaths.
- [`testing`](https://github.com/owid/covid-19-data/tree/master/public/data/testing): data from various official sources, related to COVID-19 tests performed in each country. This folder contains two files with more detailed information:
  - [`covid-testing-all-observations.csv`](https://github.com/owid/covid-19-data/blob/master/public/data/testing/covid-testing-all-observations.csv) includes, for each historical observation, the source of the individual data point, and sometimes notes on data collection;
  - [`covid-testing-latest-data-source-details.csv`](https://github.com/owid/covid-19-data/blob/master/public/data/testing/covid-testing-latest-data-source-details.csv) includes, for each country in our testing dataset, the latest figures and a detailed description of how the country’s data is collected;
- [`excess_mortality`](https://github.com/owid/covid-19-data/tree/master/public/data/excess_mortality): data on excess mortality during the pandemic, sourced from [the Human Mortality Database](https://www.mortality.org/) and [the UK Office for National Statistics](https://www.ons.gov.uk/peoplepopulationandcommunity/birthsdeathsandmarriages/deaths/articles/comparisonsofallcausemortalitybetweeneuropeancountriesandregions/januarytojune2020);
- [`vaccinations`](https://github.com/owid/covid-19-data/tree/master/public/data/vaccinations): data from various official sources, related to COVID-19 vaccinations in each country;
- [`archived`](https://github.com/owid/covid-19-data/tree/master/public/data/archived): data from other providers that we've stopped using and updating;
- [`internal`](https://github.com/owid/covid-19-data/tree/master/public/data/internal): data extracts intended for internal use at _Our World in Data_. They may change or be deleted without notice so we discourage using them.

## Data alterations

- In rare cases where our source for confirmed cases & deaths reports a _negative_ daily change due to a data correction, we set the corresponding metric (`new_cases` or `new_deaths`) to `NA`. This also means that rolling metrics (7-day rolling average, weekly rolling sum, biweekly rolling sum) are set to `NA` until this missing value leaves the rolling window.
- The population estimates we use to calculate per-capita metrics are based on the last revision of the [United Nations World Population Prospects](https://population.un.org/wpp/). The exact values can be viewed [here](https://github.com/owid/covid-19-data/blob/master/scripts/input/un/population_latest.csv). In a few cases, we use other sources (see column `source` in the population file) when the figures provided by the UN differ substantially from reliable and more recent national estimates. Population estimates for a few subnational locations are taken from national reports, and are stored [here](https://github.com/owid/covid-19-data/blob/master/scripts/input/owid/subnational_population_2020.csv).
- We standardize names of countries and regions. Since the names of countries and regions are different in different data sources, we standardize all names to the [_Our World in Data_ standard entity names](https://github.com/owid/covid-19-data/blob/master/public/data/jhu/locations.csv).
- We may correct or discard inconsistencies that we detect in the original data.
- Testing data is collected from many different sources. A detailed documentation for each country is available in [our post on COVID-19 testing](https://ourworldindata.org/coronavirus-testing#source-information-country-by-country).


## Stable URLs

The `/public` path of this repository is hosted at `https://covid.ourworldindata.org/`. For example, you can access the
CSV for the complete dataset at `https://covid.ourworldindata.org/data/owid-covid-data.csv` or the CSV with latest data
at `https://covid.ourworldindata.org/data/latest/owid-covid-latest.csv`. Note that latest data file only contains data up to 4 weeks prior the file update date.

We have the goal to keep all stable URLs working, even when we have to restructure this repository. If you need regular updates, please consider using the `covid.ourworldindata.org` URLs rather than pointing to GitHub.


## License

All visualizations, data, and code produced by _Our World in Data_ are completely open access under the [Creative Commons BY license](https://creativecommons.org/licenses/by/4.0/). You have the permission to use, distribute, and reproduce these in any medium, provided the source and authors are credited.

In the case of our vaccination dataset, please give the following citation:
> Mathieu, E., Ritchie, H., Ortiz-Ospina, E. _et al._ A global database of COVID-19 vaccinations. _Nat Hum Behav_ (2021). [https://doi.org/10.1038/s41562-021-01122-8](https://doi.org/10.1038/s41562-021-01122-8)

In the case of our testing dataset, please give the following citation:
> Hasell, J., Mathieu, E., Beltekian, D. _et al._ A cross-country database of COVID-19 testing. _Sci Data_ **7**, 345 (2020). [https://doi.org/10.1038/s41597-020-00688-8](https://doi.org/10.1038/s41597-020-00688-8)

The data produced by third parties and made available by _Our World in Data_ is subject to the license terms from the original third-party authors. We will always indicate the original source of the data in our database, and you should always check the license of any such third-party data before use.


## Authors

This data has been collected, aggregated, and documented by Edouard Mathieu, Hannah Ritchie, Lucas Rodés-Guirao, Cameron Appel, Daniel Gavrilov, Charlie Giattino, Joe Hasell, Bobbie Macdonald, Saloni Dattani, Diana Beltekian, Esteban Ortiz-Ospina, and Max Roser.

_Our World in Data_ makes data and research on the world's largest problems understandable and accessible. [Read more about our mission](https://ourworldindata.org/about).
