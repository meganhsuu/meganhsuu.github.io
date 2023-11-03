---
name: IS445_DataViz_HW8
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: This is a "showcase" project that uses vega-lite for interactive viz!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


## **Data Visualization of Building Inventory Data**

#### Viz1 - Scatter Plot by Building Status and Year Acquired

<vegachart schema-url="{{ site.baseurl }}/assets/json/HW8_chart1.json" style="width: 100%"></vegachart>

This scatter plot visualizes the relationship between "Year Acquired" and "Square Footage" for different buildings in the dataset. Each data point represents a building and is color-coded based on its "Building Status." The scatter plot allows users to explore how the year of acquisition and square footage vary across different building statuses.

Design Choices:
1. Encoding Types:
	
	The X-axis encodes "Year Acquired" as a time variable to show the distribution of acquisition years.

	The Y-axis encodes "Square Footage" as a quantitative variable to represent the size of the buildings.

	The color of the data points is encoded by "Building Status" using a nominal scale to distinguish different building statuses.

	Tooltip information includes "Building Status," "Year Acquired," and "Square Footage" to provide details on each data point when hovering.

2. Color Scheme:
The color scheme is based on a nominal scale, where each unique building status is assigned a different color. This choice helps distinguish different building statuses effectively.

3. Data Transformation:
The transform_filter method is used to filter the data based on the selected building status, which allows users to interactively explore data for a specific building status.

4. Interactivity:
The dropdown menu is provided to select a specific building status. When a status is selected from the dropdown, the plot display only the data points corresponding to that status.


#### Viz2 - Bar Chart of Building Counts by Agency Name and Building Status

<vegachart schema-url="{{ site.baseurl }}/assets/json/HW8_chart2.json" style="width: 100%"></vegachart>

This bar chart visualizes the counts of buildings for different agencies, with each bar representing a specific agency. The bars are colored based on the 'Building Status' category, and a tooltip is included to display the count of buildings for each 'Building Status' within an agency when you hover over a bar.

Design Choices:
1. Encoding Types:

	The x-axis encodes the count of buildings, providing a visual representation of the number of buildings for each agency.
 
	The y-axis encodes the 'Agency Name,' categorizing the bars by the agency. 

	The color of the bars is determined by the 'Building Status' variable. This helps distinguish the building status categories within each agency. 

	The tooltip is used to display the count of buildings ('Counts of Building') and the 'Building Status' when hovering over a bar, which provides additional information on the distribution of building statuses within each agency.

2. Color Scheme:
The color scheme is applied to the 'Building Status' variable. Different building statuses are represented by distinct colors, which makes it easier to differentiate between them in the chart.

3. Data Transformation:
The chart directly counts the number of buildings with the differentiate of 'Building Status' category for each agency. No significant data transformations are in the code.

Compare to Homework 7's Viz2, which only counted buildings by County, the new visualization focuses on counting buildings by agency and improves the chart by using different colors for building statuses, making them easier to distinguish. Tooltips are also added to show the count of buildings for each status within an agency, providing a clearer and more detailed representation of the data, and helping users explore building counts by agency and status.


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

