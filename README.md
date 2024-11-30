# Project Exploring London's Travel Network  
![tower bridge](london.jpg)

London, or as the Romans called it "Londonium"! Home to [over 8.5 million residents](https://www.ons.gov.uk/peoplepopulationandcommunity/populationandmigration/populationestimates/bulletins/populationandhouseholdestimatesenglandandwales/census2021unroundeddata#population-and-household-estimates-england-and-wales-data) who speak over [300 languages](https://web.archive.org/web/20080924084621/http://www.cilt.org.uk/faqs/langspoken.htm). While the City of London is a little over one square mile (hence its nickname "The Square Mile"), Greater London has grown to encompass 32 boroughs spanning a total area of 606 square miles! 

![underground train leaving a platform](tube.jpg)

Given the city's roads were originally designed for horse and cart, this area and population growth has required the development of an efficient public transport system! Since the year 2000, this has been through the local government body called **Transport for London**, or *TfL*, which is managed by the London Mayor's office. Their remit covers the London Underground, Overground, Docklands Light Railway (DLR), buses, trams, river services (clipper and [Emirates Airline cable car](https://en.wikipedia.org/wiki/London_cable_car)), roads, and even taxis.

The Mayor of London's office make their data available to the public [here](https://data.london.gov.uk/dataset). In this project, you will work with a slightly modified version of a dataset containing information about public transport journey volume by transport type. 

The data has been loaded into a **Snowflake** database called `TFL` with a single table called `JOURNEYS`, including the following data:  

# `Task`
Write three SQL queries to answer the following questions:

-What are the most popular transport types, measured by the total number of journeys? The output should contain two columns, 1) JOURNEY_TYPE and 2) TOTAL_JOURNEYS_MILLIONS, and be sorted by the second column in descending order. Save the query as most_popular_transport_types.  

-Which five months and years were the most popular for the Emirates Airline? Return an output containing MONTH, YEAR, and JOURNEYS_MILLIONS, with the latter rounded to two decimal places and aliased as ROUNDED_JOURNEYS_MILLIONS. Exclude null values and save the result as emirates_airline_popularity.  

-Find the five years with the lowest volume of Underground & DLR journeys, saving as least_popular_years_tube. The results should contain the columns YEAR, JOURNEY_TYPE, and TOTAL_JOURNEYS_MILLIONS.  

## TFL.JOURNEYS

| Column | Definition | Data type |
|--------|------------|-----------|
| `MONTH`| Month in number format, e.g., `1` equals January | `INTEGER` |
| `YEAR` | Year | `INTEGER` |
| `DAYS` | Number of days in the given month | `INTEGER` |
| `REPORT_DATE` | Date that the data was reported | `DATE` |
| `JOURNEY_TYPE` | Method of transport used | `VARCHAR` |
| `JOURNEYS_MILLIONS` | Millions of journeys, measured in decimals | `FLOAT` |

Note that *in Snowflake all databases, tables, and columns are **upper case*** by default.

You will execute SQL queries to answer three questions, as listed in the instructions.

# `Solution`
[sql_solution](https://github.com/jberouise2/Project-Exploring-London-s-Travel-Network/blob/222722a4bcf0df0c15599fd5b440b5fec8f18ed7/notebook.ipynb)
