
# Analysis of Affordable Housing Production by Building — 01/2020 to 03/2025

This repository contains data, analytic code, and findings that support portions of the article, “As Families Flee NYC, the City Keeps Building for Singles,” drafted April 17 2025. Please read that article, which contains important context and details, before proceeding.

## Data

This analysis uses 1 spreadsheet.

The spreadsheet comes from the following sources:

- Affordable Housing Production by Building:
  - `Affordable_Housing_Production_by_Building_20250415.csv`: Raw data of Affordable Housing Production by Building. This data set is from the Department of Housing Preservation and Development (HPD) and you can download the data in the NYC data portal [here](https://data.cityofnewyork.us/Housing-Development/Affordable-Housing-Production-by-Building/hg8x-zxpr/about_data). 

The spreadsheet contains, among others, the following columns relevant to the analysis: 

- `studio_1br` — the number of studio and one bedroom affordable housing units the city has begun work on since 1/1/2020
- `multi_bedroom` — the number of affordable housing units with more than one bedroom that the city has begun work on since 1/1/2020
- `total built units` — the total number of affordable housing units that the city has begun work on since 1/1/2020

## Methodology

The notebook [`Housing Analyis.ipynb`](notebooks/Housing Analyis.ipynb) performs the following analyses:

##### Part 1: Filtering dates to only show projects begun since January 1, 2020

- I applied a cutoff date of 01/01/2020 to the dataset, which originally began on 01/01/2014, because I wanted to see the city's work after the pandemic, which is when families began fleeing the city


##### Part 2: Making columns to show number of single occupancy and multi-occupancy units

- The dataset originally had columns for studio, 1 bedroom, 2 bedroom, 3 bedroom, 4 bedroom, 5 bedroom, and 6 bedroom+ units. I wanted to compare single vs multi-occupancy, so I maade two new columns
- I made one column summing the number of studio and 1 bedroom apartments, and another column summing the number of units with more than 2 bedrooms
- I deleted the old columns 

##### Part 3: Making a spreadsheet showing number of single occupancy and multi-occupancy units by community district 
- I used groupby to make a spreadsheet showing number of single occupancy and multi-occupancy units by community district


## Outputs

The notebooks output this spreadsheet which contains the number of single and multi-occupancy units by NYC community district: [`output/analysis.csv`](output/analysis.csv).

## Running the analysis yourself

You can run the analysis yourself. To do so, you'll need the following installed on your computer:

- Python 3
- The Python libraries specified in [`requirements.txt`](requirements.txt)

## Licensing

All code in this repository is available under the [MIT License](https://opensource.org/licenses/MIT). The data file in the output/ directory is available under the [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0) license. All files in the data/ directory are released into the public domain.

## Feedback / Questions?

Contact Quinn at quinnwaller@gmail.com.
