---
name: Healthcare Insights - Exploration of Hospital Ratings and Home Health Care
tools: [Python, HTML, vega-lite]
image: assets/pngs/heathcare_eco.png
description: A project that delivers interactive visualization experience and insights from hospital ratings and home health care data for a exploration of U.S. healthcare.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


## **Healthcare Insights - Exploration of Hospital Ratings and Home Health Care**
Group member: Megan Hsu

In the dynamic landscape of U.S. healthcare, the availability and analysis of comprehensive data play a pivotal role in shaping informed decision-making processes. This intersection of data analytics and healthcare insights is particularly exemplified through datasets focusing on hospital ratings and, furthermore, on the quality measures of home health care agencies as contextual visualization. Understanding the intricacies of these datasets is paramount for stakeholders ranging from policymakers to healthcare providers and, importantly, the general public.

### Hospital Ratings based on Hospital General Information Data

<vegachart schema-url="{{ site.baseurl }}/assets/json/FP_main_chart.json" style="width: 20%"></vegachart>

This interactive bar chart provides a comprehensive overview of mean hospital overall ratings, taking into account hospital ownership and type. Users can utilize the dropdown menu to select specific states, enabling a localized analysis. The x-axis represents mean hospital overall ratings, and the y-axis categorizes hospitals based on ownership. Color-coded bars distinguish between hospital types and the tooltip feature enhances user experience, offering detailed information on the state, hospital type, ownership, and mean hospital overall rating.

##### Potential analyses and insights
1. Regional Variations in Healthcare Quality: Users can utilize the dropdown menu to select specific states of interest. By examining the mean hospital overall ratings across various states, one can identify regional variations in healthcare quality, which can be crucial for policymakers, healthcare administrators, and the public in making informed decisions about healthcare facilities.

2. Impact of Hospital Ownership: The chart's y-axis represents different hospital ownership categories. Users can assess how hospital ownership, whether it be government-owned, non-profit, or for-profit, correlates with mean hospital overall ratings. This insight can be valuable for stakeholders looking to understand the performance of hospitals based on their ownership structures, potentially influencing healthcare policies and investments.

3. Exploration of Hospital Types: The color-coded bars represent different hospital types, such as Acute Care - Veterans Administration, Acute Care Hospitals or Critical Access Hospitals. Analyzing these categories provides insights into how specific types of hospitals contribute to the overall healthcare landscape. For instance, users can assess whether critical access hospitals tend to have higher overall ratings compared to general hospitals, offering perspectives on the diverse roles hospitals play within the healthcare system.

### Home Health Agency Ratings (Contextual Visualization)

<vegachart schema-url="{{ site.baseurl }}/assets/json/FP_line_chart.json" style="width: 100%"></vegachart>

The line chart displays the percentage of various star ratings for the quality of patient care in home health agencies of states. Users can choose a specific state from the dropdown menu, and the chart dynamically updates to show the percentage of each star rating category. This chart helps to analyze the performance of home health agencies in different regions.

##### Potential analyses and insights
1. State-wise Comparison of Patient Care Ratings: Users can employ the dropdown menu to select specific states, enabling a detailed examination of how different regions fare in terms of patient care star ratings. This facilitates a comparative analysis, helping identify states that excel or may need improvement in delivering quality patient care.

2. Correlation Between Overall Quality and Star Ratings:
By selecting a specific state, users can compare the distribution of star ratings against the overall quality of patient care. Understanding how different star ratings contribute to the overall perception of patient care quality offers a comprehensive view, guiding efforts to enhance specific aspects of healthcare services.

### Home Health Agency Quality Measures (Contextual Visualization)

<vegachart schema-url="{{ site.baseurl }}/assets/json/FP_bar_chart.json" style="width: 100%"></vegachart>

The bar chart illustrates different quality measures for home health agencies. Users can select a quality measure from the dropdown menu, and the chart displays the percentage values for home health agencies across different states. This visualization provides insights into the performance of home health agencies across different states, focusing on specific quality metrics such as patient care timeliness, physical improvement, and flu shot issues.

##### Potential analyses and insights
1. State-wise Comparison of Quality Measures: The dropdown menu allows users to select specific quality measures, facilitating a state-wise comparison. This analysis enables stakeholders to identify variations in how different states perform on key metrics related to home health care.

2. Performance Assessment Across Categories: The bar chart effectively communicates the performance of home health agencies on specific quality measures. Users can examine how agencies fare in areas such as timely patient care initiation, flu shot administration, and patient improvement in various activities. This information is crucial for evaluating and prioritizing areas for improvement within home health services.

3. Prioritizing Quality Improvement Initiatives: Stakeholders can utilize the insights gained to prioritize and tailor quality improvement initiatives. For instance, if the chart reveals a consistent challenge in a particular category across multiple states, resources and efforts can be directed towards addressing that specific aspect of home health care.

### Holistic Healthcare Decision-Making
The integrated insights from these visualizations empower stakeholders to make informed decisions that span the entire healthcare system. By synthesizing information from hospital ratings, home health agency ratings, and quality measures, users can holistically approach healthcare decision-making.

Navigating between hospital ratings and home health agency insights enables users to identify regions where both inpatient and home-based care may need targeted improvement. For example, if a state exhibits lower hospital ratings, stakeholders can correlate this with home health agency performance to pinpoint areas requiring comprehensive intervention. This integrated approach facilitates a holistic understanding of the healthcare continuum, offering a strategic lens for policymakers and administrators to implement effective, targeted improvement initiatives.

### Dataset Information
The datasets are sourced from <a href="https://data.cms.gov/provider-data">Centers for Medicare & Medicaid Services</a>.

These visualizations draw from two datasets: 
- <a href="https://data.cms.gov/provider-data/dataset/xubh-q36u">Hospital General Information</a> contains information about registered Medicare hospitals, including addresses, phone numbers, hospital types, and overall ratings. 
- <a href="https://data.cms.gov/provider-data/dataset/tee5-ixt5">Home Health Care - State by State Data</a> aggregates quality measures for home health agencies at the state level.

**Note: The Analysis button includes the python analysis notebook and the code of contextual visualization

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/meganhsuu/meganhsuu.github.io/main/Hospital_General_Information.csv" text="Hospital General Information Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/meganhsuu/meganhsuu.github.io/blob/main/python_notebooks/IS445_FinalProject.ipynb" text="The Analysis" %}
</div>

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/meganhsuu/meganhsuu.github.io/main/HH_State_Oct2023.csv" text="Home Health Care - State by State Data" %}
</div>

