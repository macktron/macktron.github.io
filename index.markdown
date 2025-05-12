---
layout: custom_home

title: "Analyzing Drug-Related Crimes in San Francisco"
---

# Introduction

![For illustrations purposes only](images/voting_polarization_USA.png)

In recent years, questions about political alignment, ideological fragmentation, and party cohesion habe become increasingly relevant within the European Union. As one of the most important legalislative bodies in the European Union, the European Parliament offers a valuable lens through which to study these evolving political dynamics.

This project uses data obtained from VoteWatch Europe, an independent organization that tracks and curates etailed information on the voting behavior of MEPs. Covering all recorded roll-call votes between 2004 and 2022, the dataset includes individual voting records as well as contextual metadata about the legislative proposals themselves.

The roll-all votes detail how each member of the European Parliament (MEP) voted on individual areas of leglislation, e.g. whether they voted for, against abstained. These records are enriched with metadata such as the MEP’s country, national party, and European Parliamentary Group (EPG).

The aim of the analysis of long-term trends in parliamentary voting behaviour will help identify shifts in consensus and division across parties, time periods, and policy areas. This project seeks to reveal how political structures within the European Union are evolving by systematically studying the outcomes and alignments within the European Parliament.

The goal is to present these findings through intuitive, interactive visualizations that allow you the reader to explore voting patterns in depth. The aim is to make it easier to detect trends in polarization, assess party cohesion, and understand which policy domains generate the most division or consensus. Ultimately, the project is intended to support a clearer, data-driven understanding of European parliamentary politics.



# European Parliament Groups (EPGs)
Within the European Parliament, Members of the European Parliament (MEPs) are organized into transnational political groups called European Parliament Groups (EPGs). These groups bring together national parties from different EU countries that share similar political ideologies.

In our analysis, we focus on how these EPGs vote on different policy issues, as shifts in their voting patterns can reveal important insights about political alignment, cohesion, and change within the EU.

![Rice Index](images/epg_table_bokeh.png)



### Measure of political polarizatoin


Since **polarization** is a fairly abstract term, we need to **quantify** it somehow. Since we have the voting results of all MEPs, we can use them to measure the agreement within groups as a metric of polarization.

To do this, we use the **Rice Index**, which is a number between 0 and 1 that indicates the level of agreement within a group. The formula is:



![Rice Index](images/rice_index.png)

Where:

* **Y** is the number of votes in favor (Yes),
* **N** is the number of votes against (No),
* **A** is the number of abstentions.




# Clustering of EPG simmilarity

<div style="display: flex; justify-content: center; margin: 0; padding: 0; line-height: 0;">
  <iframe 
    src="/images/epg_clustering_combined.html"
    style="width: 90vw; max-width: 1000px; height: 200px; border: none; display: block; margin: 0; padding: 0;"
    loading="lazy">
  </iframe>
</div>

# Clustering of EPG simmilarity


### Policy Areas###
Each legislative vote in the European Parliament is associated with a policy area; a thematic classification that indicates the primary subject or focus of the vote. These categories help structure the vast range of EU legislative activity and are used by parliamentary committees and documentation systems to track and organize legislation. Policy areas range from broad domains like environment, budget, and foreign affairs to more specific issues such as digital regulation or public health. They serve as an important analytical layer for understanding what kinds of issues are being voted on, how often they arise, and how political divisions manifest across different types of legislation.

To help understand the nature of political alignment and divvision within the European Parliament, the roll-call votes categorized by legislative topic. Each voote is tagged with a policy area that describes its sustantive focus, allowing us to analyze trends within and across issue domains. These include:
['budgetary control', 'agriculture', 'culture education', 'development', 'employment social affairs', 'environment public health', 'fisheries', 'gender equality', 'international trade', 'legal affairs', 'regional development']

* **Budgetary Control** This policy  focuses on overseeing how the European Union’s budget is spent. It includes votes on the discharge of annual budgets, audits of EU institutions, reports on financial irregularities, and recommendations for improved fiscal oversight. MEPs use these votes to examine and evaluate spending by the European Commission, European agencies, and other bodies to ensure accountability, transparency, and adherence to EU rules. While often technical, this domain reflects deeper political debates about institutional trust and financial governance.


* **Agriculture**
Agricultural policy is primarily governed through the Common Agricultural Policy (CAP), one of the EU's largest and most influential frameworks. This area includes votes on subsidies for farmers, environmental conditions for aid, food production standards, and rural development strategies. The topic frequently highlights tensions between environmental sustainability, food security, and economic support for agricultural communities. It also brings into focus national interests, as agricultural priorities vary widely across member states.

* **Gender Equality**
This policy focuses on eliminating discrimination and promoting fair treatment regardless of gender. MEPs vote on initiatives such as closing the gender pay gap, combatting gender-based violence, increasing female representation in political and corporate leadership, and ensuring work-life balance. These votes often intersect with broader debates on social justice, cultural norms, and human rights, with varying levels of support across political and regional lines.

* **International Trade**
This area involves the EU’s commercial relationships with non-EU countries, including trade agreements, tariff policy, and regulatory cooperation. Votes often concern major trade deals (e.g., with Canada, Japan, or Mercosur), export controls, and trade sustainability clauses. This policy area illustrates ideological splits between support for liberalized global markets and calls for stronger protections for labor rights, environmental standards, and strategic industries.

* **Fisheries**
This area is governed by the Common Fisheries Policy (CFP), this domain includes legislation on the sustainable management of marine resources, fishing quotas, fleet regulation, and cooperation with non-EU countries on fishing rights. Fisheries policy is vital for coastal economies and often involves negotiations between ecological goals (e.g., preventing overfishing) and economic pressures from national fishing industries. This area can reveal regional divides, especially among member states with significant maritime sectors.

* **Employment & Social Affairs**
This topic covers EU legislation on labor markets, workers' rights, social protections, and inclusive employment policies. Votes address issues such as working conditions, minimum wages, occupational health and safety, social security coordination, and labor mobility. This area is ideologically charged, with progressive and centrist parties typically supporting stronger labor protections, while others advocate for labor market flexibility and reduced regulation.

* **Environment & Public Health**
A high-priority and expansive domain, this area includes votes on environmental regulation (e.g., climate change, biodiversity, pollution control) and health-related policies (e.g., pandemic preparedness, food safety, cross-border healthcare). MEPs debate legislative proposals aiming to balance ecological sustainability and public well-being with economic interests. Disagreement often arises over regulatory stringency, climate targets, and the role of innovation in solving environmental challenges.

* **Development**
Development policy focuses on the EU’s engagement with lower-income countries through humanitarian aid, technical assistance, and economic partnerships. MEPs vote on funding for global development projects, EU contributions to international organizations, and programs promoting democracy, gender equality, education, and poverty reduction. The topic reflects the EU’s identity as a normative global actor and often connects to broader foreign policy and trade agendas.

[**Reference for EU Policies**](https://www.europarl.europa.eu/topics/en/all)

## Clustering of EPG simmilarity over policy areas


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

