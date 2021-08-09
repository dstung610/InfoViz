# World Inequality Index (2019-wid)
**This README will give the information about the authors and the explanation that needed regarding all the visualizations that are presented in our project.**



## Students
* Arieta Shabani
* Mirjeta Shabani
* Mohamad Hamamah
* Son-Tung Do

## Data (Extracts of the [World Inequality Database](https://wid.world/))
* **data/** the data in [tsv](https://bl.ocks.org/mbostock/3305937).
	* **countries.tsv** country codes
	* **income/** income share per country
	* **income-gini.tsv** gini index
	* **income-average.tsv** average income
* **viz/** sample visualisations
* **vendor/** vendorized d3 library

## Deployment
Extract the zip package and navigate to the extracted directory and launch python web server
```
// Depend on your python version use either following command
python3 -m http.server
python -m http.server
```
Then access the directory via web browser with
`localhost:8000`

When we access in address, navigate over the the `viz/` folder and select one of the visualization that we have implemented.

## Visualizations

##### 1. Income Distribution Histogram
To access this visualization go in `/viz/distribution_graph.html`.

| Data | Visual variables |
|----|----|
|Population Share| Position|
|Share of income per population| Position |
|Time | High cognitive components (slider selection) |
|Country | High cognitive components (dropdown selection) |

Interactions that are implemented in this visualization has the following

* X axis is scaled based the selected lower bound for x axis
* Choosing a country from the dropdown menu shows the data for the corresponding choice
* Time slider enable chossing the year for which to display the data
##### 2. Geo-map
To access this visualization go in `viz/geo-map.html`.

| Data | Visual variables |
|----|----|
|Countries| Position |
|Quantiles| High cognitive components (dropdown selection)|
|Years| High cognitive components (dropdown selection)|
|Quantile value| Color gradient |

There are 2 interactions that are implemented in this visualization

* Hover over a country, there will be a tooltip that indicate the name of the country along with the share of the income in a specific year. Simultaneously, a indicator is shown along the legend to help user see the range that it multilines
* Hover over the legend, on each gradient cell (if available), there will be a highlight to all the countries that hold that value. For example, based on the data we have, we can try 0.7 share in the year 1995, it should return 3 different ranges: 20-30%, 30-40%, and 40-50%.

In the same fashion, we change the data of gini index to do it.
Accessing this visualization in `viz/geo-map-gini.html`
##### 3. Gini line graph
To access this visualization go in `viz/gini.html`

| Data | Visual variables |
|----|----|
|Time|X-axis|
|Value|Y-axis|
|Countries|High cognitive components (checkbox selection)|
|Evolution|Line and color|

Interactions that are implemented in this visualization has the following

* Time (X-axis) is scaled based on the min and max of the current countries selected
* To avoid confusion in this visualization, we only allow to have a maximum of 5 countries to be selected. Along with this selection, legend also added to have more clear instruction of which color has been encoded to which country

##### 4. Gini world wide view
To access this visualization go in `viz/geo-map-gini.html`

| Data | Visual variables |
|----|----|
|Gini value| Hue|
|Countries| Position|
|Years| High cognitive components (dropdown selection)|

There are 2 interactions that are implemented in this visualization

* Hover over a country, there will be a tooltip that indicate the name of the country along with the gini value a specific year. Simultaneously, a indicator is shown along the legend to help user see the range that it multilines
* Hover over the legend, on each gradient cell (if available), there will be a highlight to all the countries that hold that value.
