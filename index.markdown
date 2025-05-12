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

The aim of the analysis of long-term trends in parliamentary voting behaviour will help identify shifts in consensus and division across parties, time periods, and policy areas. This project seeks to reveal how political structures within the European Union are evolving by systematically studying the outcomes and alignments within the European Parliament.

The goal is to present these findings through intuitive, interactive visualizations that allow you the reader to explore voting patterns in depth. The aim is to make it easier to detect trends in polarization, assess party cohesion, and understand which policy domains generate the most division or consensus. Ultimately, the project is intended to support a clearer, data-driven understanding of European parliamentary politics.


## Eupean Parliment Groups

Within the european parliment there are coaliattion within the parlinent over different natinaliteis and natinal parties. We will look a lot on these voitng patters sicne we think how they change their voting patters will give us many insights about

<div style="display: flex; justify-content: center; margin: 0; padding: 0; line-height: 0;">
  <iframe 
    src="/images/epg_table_bokeh.html"
    style="width: 90vw; max-width: 1000px; height: 700px; border: none; display: block; margin: 0; padding: 0;"
    loading="lazy">
  </iframe>
</div>




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




## Clustering of EPA simmilarity

<div style="display: flex; justify-content: center;">
  <iframe 
    src="/images/epg_clustering_combined.html"
    style="width: 90vw; max-width: 1000px; height: 700px; border: none;"
    loading="lazy">
  </iframe>
</div>



### Policy Areas###
Each legislative vote in the European Parliament is associated with a policy area; a thematic classification that indicates the primary subject or focus of the vote. These categories help structure the vast range of EU legislative activity and are used by parliamentary committees and documentation systems to track and organize legislation. Policy areas range from broad domains like environment, budget, and foreign affairs to more specific issues such as digital regulation or public health. They serve as an important analytical layer for understanding what kinds of issues are being voted on, how often they arise, and how political divisions manifest across different types of legislation.

To help understand the nature of political alignment and divvision within the European Parliament, the roll-call votes categorized by legislative topic. Each voote is tagged with a policy area that describes its sustantive focus, allowing us to analyze trends within and across issue domains. These include:
['budgetary control', 'agriculture', 'culture education', 'development', 'employment social affairs', 'environment public health', 'fisheries', 'gender equality', 'international trade', 'legal affairs', 'regional development']

* **Budgetary Control** This policy  focuses on overseeing how the European Union’s budget is spent. It includes votes on the discharge of annual budgets, audits of EU institutions, reports on financial irregularities, and recommendations for improved fiscal oversight. MEPs use these votes to examine and evaluate spending by the European Commission, European agencies, and other bodies to ensure accountability, transparency, and adherence to EU rules. While often technical, this domain reflects deeper political debates about institutional trust and financial governance.







## Clustering of EPA simmilarity over policy areas


<div style="display: flex; justify-content: center;">
  <iframe 
    src="/images/epg_clustering_per_policy_area.html"
    style="width: 90vw; max-width: 1000px; height: 700px; border: none;"
    loading="lazy">
  </iframe>
</div>





## Yearly voting heatmap

Based on percentage of yes votes in areas

<div style="display: flex; justify-content: center;">
  <iframe 
    src="/images/ep_voting_yearly_heatmap.html"
    style="width: 90vw; max-width: 1000px; height: 700px; border: none;"
    loading="lazy">
  </iframe>
</div>

