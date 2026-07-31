# ME204 Final Project: [Your project title]


| GitHub username                           | LSE ID            |
| ----------------------------------------- | ----------------- |
| `[username]`                              | `2026201945758`        |


Remove the unused row if you work alone.
Replace every `[bracketed]` placeholder once you fill it in.

## Overview

The study is an exploratory analysis of conflict events in Syria since the fall of the Assad regime on 8 December 2024, up until today (cutoff 20 July 2026).

## Data sources

For the study I drew on data from ACLED which is a highly reutable resource for accessing data on conflict events worldwide. They gather data via a mix of media channels. 

Their API is accessible to users who register with an institutional email address, principally including academic institutions too. An older version of their documentation states that academic users can make a maximum of 6000 calls. Since the Syria dataset is large and requires pagination, the API in the notebook specifies the date from when data should be collected, to limit the number of calls (as of July 2026 it should return 4 pages of raw data). Each page contains maximum 5000 records. This is reflected in the code to collect data in NB01 in the 'break' statement. When the 'data' key in the json object contains less than 5000 entries, it has reached the end of the dataset.

ACLED provides the code to set up and apply the authentication token to be able to access the data, which is found in Notebook 1. 

For further information about ACLED's API, please refer to their website: https://acleddata.com/acled-api-documentation

The dataset comes somewhat pre-filtered as the columns of potential interest are specified in the params section of the url that is used to make the call.


## How to reproduce

To access the API, use the code that ACLED provides, which is also replicated in NB01. 

From there on, each notebook runs from top to bottom, but it is advisable to run some snippets in bulk instead of the entire script, in case a snippet malfunctions.

Notebooks NB03a-c are a bit jumbled; there is some overlap among them, especially NB03a and NB03b. The analysis in NB03a ends quite abruptly and picks up again in NB03b. This should not present any issues to running the code however, but some parts of the code may look like dead ends. Most of the more insightful charts are produced in NB03c.

The findings are presented on the website linked to this project: https://anjsel.github.io/final-project-me204-new-repos/ 

