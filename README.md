# Assessing the Impact of Affordable Housing Development

In the last decade, Davidson County has experienced tremendous population growth. With this population growth has come skyrocketing housing costs. From 2010 to 2019, both home values and rents have grown by more than 150%, while wages increased only slowly. High housing costs can squeeze household budgets, reducing the money available for other daily needs, including food, clothing, health care, utilities, and transportation, as well as money needed for education or for future savings.

One method of addressing rising housing costs is by building affordable housing developments. Despite the potential benefits, property owners who live near proposed housing developments often oppose such projects, citing fear that the developments will cause their property values to decline or will increase crime rates.

In this project, you'll be examining the impact of housing units built in Davidson under the the Low Income Housing Tax Credit (LIHTC) or which were funded by the [Barnes Housing Trust Fund](https://www.nashville.gov/departments/mayor/housing/barnes-fund). Established in 1986, the LIHTC program has become an integral component of federal housing policy, funding 21 percent of all multifamily developments over the period 1987-2008. The Barnes Fund, created in 2013, is Metro Nashville's first housing trust fund and was created to leverage affordable housing developments throughout Davidson County.

You have been provided with several data sources:

* housing.backup: A database containing information on all parcels in Davidson County. This database was scraped from https://maps.nashville.gov/ParcelViewer/.
    - The sales table contains the sales transaction history of each property. Warning - in a lot of cases, the sales price is $0, so filter out these cases.
    - The locations table contains the centroid of each parcel, which can be used to determine distance to each housing development.
* LIHTC.csv: Contains information on all Davidson County developments from the Department of Housing and Urban Development (HUD) National Low Income Housing Tax Credit Database.

    - For more information about the variables contained in this dataset, see the included data dictionary

* barnes.csv: Contains information on rental properties that are completed and have more than 10 units which were funded by the Barnes Fund.
    - Note that there is some overlap between the first and second dataset.

* census.sqlite: Contains data gathered from the US Census [American Community Survey](https://www.census.gov/data/developers/data-sets.html) for the years 2009 through 2020.
    - For the tables and variables included, see the data dictionary.

For your analysis, focus on residential properties.

Questions:
1. What is the general trend in sales prices by census tract over the last 10 years? **In which areas of Davidson County are sales prices increasing at the highest rate?** Census tract is contained in the tract column of the properties table.
2. **Is there any difference in the change in home prices for tracts that contained an affordable housing development compared to those which did not?** Is this impact different for tracts with a higher or lower median income level? (Median income is contained in the B19013 table of the census database).
3. Find **homes which were sold at least two times**. For each such home, find the distance to the nearest affordable housing development. **Does distance to an affordable housing development seem to have any effect on the sales price increase for homes which were sold both before and after a development was put into service?**

Stretch Goals:
* Analyze the demographics of the areas in which home prices are increasing the fastest. How did the demographics of these areas change? Building off of this, how do the demographics of areas which had an affordable housing development compare to those that did not have one?
* You have also been given police_incidents.csv, which contains all police incidents reported on https://data.nashville.gov/Police/Metro-Nashville-Police-Department-Incidents/2u6v-ujjs from 2015 through the November of 2022. For more information and a data dictionary, see the metadata pdf. Using this data, compare the amount of crime before and after an affordable housing development. Look at the two-to-three years before and after. Is there any increase in overall crime rate? Does the rate of any particular crime increase near affordable housing developments?
