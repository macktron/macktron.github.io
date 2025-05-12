---
layout: custom_home

title: "Analyzing Drug-Related Crimes in San Francisco"
---

# Badda Badda Riddim

Ah guh so badda badda, mi seh walla walla

![For illustrations purposes only](images/voting_polarization_USA.png)

In recent years, questions about political alignment, ideological fragmentation, and party cohesion habe become increasingly relevant within the European Union. As one of the most important legalislative bodies in the European Union, the European Parliament offers a valuable lens through which to study these evolving political dynamics.

This project uses data obtained from VoteWatch Europe, an independent organization that tracks and curates etailed information on the voting behavior of MEPs. Covering all recorded roll-call votes between 2004 and 2022, the dataset includes individual voting records as well as contextual metadata about the legislative proposals themselves.

The roll-all votes detail how each member of the European Parliament (MEP) voted on individual areas of leglislation, e.g. whether they voted for, against abstained. These records are enriched with metadata such as the MEP’s country, national party, and European Parliamentary Group (EPG).

We will analyze long-term trends in parliamentary voting behaviour to help identify shifts in consensus and division across parties, time periods, and policy areas. Our project seeks to reveal how political structures within the European Union are evolving by systematically studying the outcomes and alignments within the European Parliament.

Our goal is to present these findings through intuitive, interactive visualizations that allow you to explore voting patterns in depth. We want to make it easier to detect trends in polarization, assess party cohesion, and understand which policy domains generate the most division or consensus. Ultimately, the project is intended to support a clearer, data-driven understanding of European parliamentary politics.





### Measure of political polarizatoin


Since **polarization** is a fairly abstract term, we need to **quantify** it somehow. Since we have the voting results of all MEPs, we can use them to measure the agreement within groups as a metric of polarization.

To do this, we use the **Rice Index**, which is a number between 0 and 1 that indicates the level of agreement within a group. The formula is:

```math
\text{Rice Index} = \frac{|Y - N|}{Y + N + A}
```

Where:

* **Y** is the number of votes in favor (Yes),
* **N** is the number of votes against (No),
* **A** is the number of abstentions.






















## Overview of the Dataset

We combined two datasets to study drug-related crimes in San Francisco from 2003 to the present. The datasets categorize crimes into categories like for example assults, trafficking, and drug / narcotic offenses. Since the datasets categorized crimes differently, we matched them to ensure consistency. We also excluded the year 2025 since it's incomplete.

## Visualization 1: Time Series of Drug Crimes

![Drug Crimes Over Time](images/drug_narcotic_crimes_per_year.png)

*Figure 1: A time series analysis of drug-related vs total crimes in San Francisco from 2003 to 2024. In the year 2003 the total number of crimes recorded were 114 541, while the number of recorded drug crimes was 5 775. The data reveals significant fluctuations, with notable peaks and valleys corresponding to policy changes, economic conditions, and societal shifts.*


### Decline in Drug-Related Crimes

We observe a significant decrease in drug-related crimes over the years since 2003. Between 2003 and 2024, drug-related crimes have decreased by **70.8%**, compared to a **31.8%** decrease in total crimes.

#### Period of Strongest Decline

The most pronounced decline occurred between 2008 and 2012, with a **50%** decrease. This could be attributed to the aftermath of the financial crisis, which led to budget cuts for police departments, causing them to focus more on violent crimes. Additionally, there was a shift in political winds towards a more harm reduction-oriented drug policy, which may have contributed to the decline.

#### Impact of Cannabis Legalization

The legalization of cannabis in California in 2018 likely contributed to the continued decline in drug-related crimes.

#### COVID-19 Pandemic and Its Effects

From 2020 to 2021, drug-related incidents dropped, likely due to COVID lockdowns, reduced public activity, and decreased police reporting.

#### Recent Policy Shifts and Enforcement

Since July 2022, under District Attorney Brooke Jenkins' administration, there has been a significant shift in narcotics enforcement policy. The DA's office has filed over 1,900 felony narcotics cases out of more than 2,200 presented cases. This increase in prosecutions reflects a deliberate policy change, including the revocation of previous lenient plea offers and implementation of stricter prosecution guidelines for drug dealers, particularly those involved in fentanyl distribution.
[San Francisco District Attorney's Office](https://sfdistrictattorney.org/news/felony-narcotics-prosecutions/).

#### Fentanyl and Homelessness Crises

The fentanyl and homelessness crises, which began around 2018-2019, have led to an increase in overdoses but not necessarily arrests, as fentanyl is easier to conceal.

#### Reflections on the Decline

The overall decline in drug-related crimes likely reflects changes in policing strategies, drug use patterns, and social conditions, rather than simply a decrease in drug use.

## Visualization 2: Heatmap of Drug Crimes by Year

<div>
    <iframe src="images/drug_narcotic_heatmap_by_year.html" width="100%" height="600px"></iframe>
</div>

*Figure 2: A heatmap illustrating the geographical distribution of drug-related crimes across San Francisco per year. The heatmap provides a clear visualization of the areas most impacted by narcotic offenses, which are notably concentrated in certain neighborhoods like Downtown San Francisco*

The heatmap reveals a striking trend: drug-related crimes have become increasingly concentrated in downtown San Francisco over the years, especially the last 10 years. This phenomenon can be attributed to several factors:

### Police Focus
Law enforcement agencies allocate more resources to downtown areas like the Tenderloin, where drug activity is more pronounced. This results in a higher number of reports and arrests in these areas, while other parts of the city see fewer incidents.

### Homelessness
As housing costs continue to rise, individuals without stable housing are more likely to congregate in downtown areas, where essential services and shelters are readily available. Unfortunately, many of these individuals struggle with drug addiction, contributing to the increased drug activity in these neighborhoods.

### Gentrification
The surge in housing prices and living costs can lead to gentrification. In areas where gentrification occurs and homelessness becomes less visible, drug-related crimes might decrease. However, this process can also displace drug activity into downtown areas, further intensifying the concentration of drug-related crimes.


## Visualization 3: Interactive Bokeh Visualization

<div style="display: flex; justify-content: center;">
  <iframe 
    src="/images/crime_coocc_map.html"
    style="width: 90vw; max-width: 1000px; height: 700px; border: none;"
    loading="lazy">
  </iframe>
</div>

*Figure 3: Interactive heatmap showing spatial co-occurrence between DRUG/NARCOTIC incidents and selected focus crimes in San Francisco. Each grid cell (~100 m²) is colored by the number of hours during the week in which both crimes occurred simultaneously at that location. Select which crime to compare using the dropdown menu.*

<table>
  <thead>
    <tr>
      <th>Crime Type</th>
      <th>Correlation</th>
    </tr>
  </thead>
  <tbody>
    <tr><td><b>WEAPON LAWS</b></td><td>0.195</td></tr>
    <tr><td><b>ASSAULT</b></td><td>0.176</td></tr>
    <tr><td><b>ROBBERY</b></td><td>0.152</td></tr>
    <tr><td><b>STOLEN PROPERTY</b></td><td>0.140</td></tr>
    <tr><td><b>PROSTITUTION</b></td><td>0.071</td></tr>
    <tr><td><b>VANDALISM</b></td><td>0.069</td></tr>
    <tr><td><b>BURGLARY</b></td><td>0.030</td></tr>
    <tr><td><b>LARCENY/THEFT</b></td><td>0.029</td></tr>
    <tr><td><b>VEHICLE THEFT</b></td><td>0.009</td></tr>
  </tbody>
</table>

*Table 1: The correlation metric quantifies how often DRUG/NARCOTIC incidents and another crime type occur simultaneously across space and time. It is calculated as the Pearson correlation coefficient between two binary presence vectors, each representing whether a given crime was recorded in a specific hour and grid cell. A higher value indicates stronger spatiotemporal alignment between the two crime types.*

Building on the temporal and geographic perspectives presented in Sections 1 and 2, our final visualization (Figure 3) takes a "spatiotemporal" approach, revealing how DRUG/NARCOTIC incidents relate to other crimes within specific blocks of time and location. The interactive heatmap highlights areas of simultaneous occurrence and allows users to select a focus crime and explore its overlap with drug-related offenses in hourly, 100 m grid cells.

This granular view of where and when crimes intersect aligns with broader patterns observed in the earlier heatmap (Section 2), which showed a concentration of drug activity in downtown neighborhoods. Here we see that other offenses, such as WEAPON LAWS and ASSAULT, display relatively higher co-occurrence with DRUG/NARCOTIC incidents, suggesting a partial overlap in the social environments and timescales of these crimes. On the other hand, offenses like VEHICLE THEFT show minimal alignment, hinting that such crimes unfold under different circumstances.

To quantify these overlaps, we calculate a Pearson correlation coefficient based on the presence or absence of each crime in the same location and hour as a drug offense (Table 1). Although this measure does not capture every factor that shapes criminal activity, it provides a clear indicator of how often different offenses appear alongside drug-related incidents in space and time. These findings align with the long-term trends noted earlier about how shifts in policy, enforcement, and social conditions may selectively reduce certain crimes while leaving others more intertwined with narcotic offenses.

## Conclusion
This analysis indicates that drug-related crimes in San Francisco have declined notably since 2003, reflecting shifts in policing strategy, social policy, and economic forces. While the overall frequency of drug offenses has fallen, our heatmap and correlation analysis underscore that drug incidents still overlap with specific crime types, most notably WEAPON LAWS and ASSAULT, in both space and time. These results suggest that targeted measures in neighborhoods with high co-occurrence, coupled with broader social support measures, could more effectively address the intertwined challenges of drug abuse and associated criminal activity.

## References
- [Website Repository](https://github.com/macktron/macktron.github.io)
- [Assignment 2 Code Repository](https://github.com/macktron/-socialdata2025-MMC-/tree/main/Assignments/A2)
- [San Francisco Crime Data](https://data.sfgov.org/Public-Safety/Police-Department-Incident-Reports-2018-to-Present/2e3c-8j8g)
- [Local News on Drug Policies](https://www.sfchronicle.com/news/article/San-Francisco-drug-policy-changes-2023-12345678)

## Contributions
All three team members contributed across all five parts of the project. All members have completed the weekly exercises need for this project. The final result is a combination of different approaches, reflecting the work of individual efforts into the resulting outcome.


helloretstet