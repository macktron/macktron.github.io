---
layout: custom_home

title: "Analyzing Polarization in the European Parliament"
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


<div style="display: flex; justify-content: center; margin: 0; padding: 0; line-height: 0;">
  <iframe 
    src="/images/epg_table_bokeh.html"
    style="width: 120vw; max-width: 1000px; height: 700px; border: none; display: block; margin: 0; padding: 0;"
    loading="lazy">
  </iframe>
</div>



# Political polarization within EPGs


Since **polarization** is a fairly abstract concept, we need a way to **quantify** it. Fortunately, because we have the voting records of all Members of the European Parliament (MEPs), we can measure the level of agreement within political groups as an indicator of polarization.

A common metric for internal group agreement is the **Rice Index**, which produces a score between 0 and 1. This gives a simple, quantifiable measure of how unified a group is in its voting behavior. [Learn more about the Rice Index](/riceindex/).







# Political polarization between EPGs

When we want to understand the **similarity in voting behavior between two different political groups (EPGs)**, the Rice Index falls short. It only looks at agreement within a single group and doesn't consider differences in group size or how often members abstain.

To address this, we use a **custom agreement index** that compares how two groups distribute their votes (Yes, No, Abstain). It calculates how similar their voting patterns are—adjusting for size differences—and returns a value between 0 and 1, where 1 means identical voting behavior. [Learn more about the Custom Index](/customindex/).


With this method, we can see how similarly each group in the European Parliament (EPGs) voted. We use this information to make a low dimensional map where each group is a point. Groups that voted in similar ways appear closer together on the map, while those that voted differently are farther apart. This map is created using a technique called PCA, which helps us show complex patterns in just two dimensions.

<div style="display: flex; justify-content: center; margin: 0; padding: 0; line-height: 0;">
  <iframe 
    src="/images/epg_clustering_combined.html"
    style="width: 90vw; max-width: 1000px; height: 700px; border: none; display: block; margin: 0; padding: 0;"
    loading="lazy">
  </iframe>
</div>


The clustering of political groups (EPGs) based on voting similarity shows clear and consistent alignment between the **Greens/EFA** and **The Left** throughout the observed period. These two groups maintain close proximity in the map, suggesting strong overlap in their voting behavior on most issues. Similarly, **S\&D** and **Renew Europe (REG)** often appear near each other, indicating shared legislative priorities despite being separate blocs.

In contrast, the **Identity and Democracy Group (IDG)** is consistently distant from other EPGs. This persistent separation suggests systematically divergent voting behavior, likely rooted in its far-right ideological position. This is in line with prior research showing that radical-right parties often isolate themselves from consensus-based voting blocs in the European Parliament (McDonnell & Werner, 2020).

**Non-attached MEPs** (NI) are also found in isolated positions in the similarity maps, though with more variability. This reflects their heterogeneous composition—many are either independent, represent niche national interests, or are affiliated with parties excluded from formal EPGs.

From 2019 to early 2020, the clustering remains relatively stable, with only minor shifts in group positions. However, starting around **2020**, there is a visible increase in **polarization**. Notably, **IDG and EPP** drift further apart, while **REG** also begins to distance itself from the central alignment cluster formed by S\&D and Greens/EFA. This coincides with the **COVID-19 pandemic**, which introduced unprecedented legislation and emergency measures. The crisis likely sharpened ideological divides, especially on issues related to civil liberties, public spending, and EU-level coordination—areas where right-wing and centrist parties often diverge.

In the post-pandemic period, the distance between EPGs continues to widen gradually, suggesting a long-term fragmentation trend. This could reflect broader political shifts in the EU, including the rising influence of nationalist parties, debates over green transition policy, and growing disagreement over migration and digital regulation.

Overall, the data suggest a pattern of increasing divergence between ideological extremes and the centrist bloc, particularly since 2020. The observed dynamics align with wider concerns about democratic backsliding and reduced cross-party consensus in EU governance.



# Policy Area
Each legislative vote in the European Parliament is associated with a policy area; a thematic classification that indicates the primary subject or focus of the vote. These categories help structure the vast range of EU legislative activity and are used by parliamentary committees and documentation systems to track and organize legislation. Policy areas range from broad domains like environment, budget, and foreign affairs to more specific issues such as digital regulation or public health. They serve as an important analytical layer for understanding what kinds of issues are being voted on, how often they arise, and how political divisions manifest across different types of legislation.

To help understand the nature of political alignment and divvision within the European Parliament, the roll-call votes categorized by legislative topic. Each voote is tagged with a policy area that describes its sustantive focus, allowing us to analyze trends within and across issue domains. These include:

<details>
  <summary> Budgetary Control</summary>
  This policy  focuses on overseeing how the European Union’s budget is spent. It includes votes on the discharge of annual budgets, audits of EU institutions, reports on financial irregularities, and recommendations for improved fiscal oversight. MEPs use these votes to examine and evaluate spending by the European Commission, European agencies, and other bodies to ensure accountability, transparency, and adherence to EU rules. While often technical, this domain reflects deeper political debates about institutional trust and financial governance.
</details>

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






## 1. Parliament-wide Agreement

<div style="display: flex; justify-content: center;">
  <iframe 
    src="/images/01_parliament_agreement.html"
    style="width: 90vw; max-width: 1000px; height: 500px; border: none;"
    loading="lazy">
  </iframe>
</div>

This line chart shows the annual average Rice index for **all** roll-call votes. The x-axis runs from the earliest full year in our dataset to the most recent, and the y-axis show the Rice index illustrating the division between 0 (maximum division) and 1 (complete unity).  A hover tooltip reveals the exact Rice value for each year.

### 1.2 Interpretation of General Agreement 
The graph shows a maximum variation of about 20 %. Looking at the "spikes" and thus the periods with most disagreement.
The Rice index exhibits two pronounced peaks over the 2005–2021 period, both coinciding with systemic crises. In 2008, the index quickly rose from approximately 0.5 to 0.63, reflecting broad cross-group endorsement of emergency financial-stability measures during the global banking collapse. Following this a gradual decline ensued—reaching a trough near 0.47 by 2019—driven by intensifying sovereign-debt disputes, the expansion of populist and Eurosceptic factions, and the polarization induced by the Brexit debate. [**BrexitPlorizing**](https://www.gisreportsonline.com/r/brexit-society-europe/)

With the COVID-19 pandemic in early 2020, the Rice index rose again and climbed from roughly 0.48 to 0.54 as MEPs coalesced around the €750 billion NextGenerationEU recovery fund, joint vaccine procurement and health-emergency protocols. [**EU**](https://commission.europa.eu/strategy-and-policy/recovery-plan-europe_en) In both instances the data indicate that extreme external shocks substantially increase legislative cohesion and in inter-crisis intervals, the ideological and national-interest have higher value.


## 2. Polarization by Policy Area
<div style="display: flex; justify-content: center;">
  <iframe 
    src="/images/agreement_by_policy_area_interactive.html"
    style="width: 90vw; max-width: 1000px; height: 500px; border: none;"
    loading="lazy">
  </iframe>
</div>

An interactive multi-select chart overlays the average line in black with colored lines for each policy domain (e.g. fisheries, budgetary control, internal market). Hovering over any point shows (Policy Area, Year, Rice). You can add or remove areas to compare their dynamics against the overall trend.

### 2.2 Identify the Most Polarizing Domains  
*(to be filled in once variance rankings are computed; here note which areas stray furthest from the average and when.)*

### 2.3 Underlying Drivers  
Some policy domains are inherently more contentious:

- **Economic vs. social regulation.** Internal market and budgetary file votes may assemble broad majorities, whereas social affairs or welfare reforms can cleave national party lines.  
- **Sovereignty issues.** Justice & Home Affairs, constitutional affairs, or enlargement debates often split pro- and anti-federalist forces.  
- **Interest-group pressure.** Agriculture, fisheries, and environmental files see intense lobbying from sectoral stakeholders, driving MEPs to break from their party if domestic interests call for it.  

Exploring the most variable policy areas will help us diagnose what kinds of issues drive the Parliament’s cohesion up or down.

---

## 3. Within-Party Cohesion
<div style="display: flex; justify-content: center;">
  <iframe 
    src="/images/02_within_party_agreement.html"
    style="width: 90vw; max-width: 1000px; height: 500px; border: none;"
    loading="lazy">
  </iframe>
</div>

### 3.1 Chart: Rice Index by Party Over Time  
This interactive line chart plots one line per political group (EPP, S & D, Greens/EFA, The Left, etc.), each initially visible but toggleable via checkboxes. It reveals which parties remain tightly unified across years and which show the greatest internal splits.

### 3.2 Observations  
*(to be filled once the lines are drawn; note which parties are most/least cohesive and how their trajectories compare.)*

### 3.3 Bar Chart: Party Disagreement by Policy Area  
<div style="display: flex; justify-content: center;">
  <iframe 
    src="/images/04_bar_rice_by_policy_and_party.html"
    style="width: 90vw; max-width: 1000px; height: 500px; border: none;"
    loading="lazy">
  </iframe>
</div>

A dropdown-controlled bar chart shows, for the selected party, its average Rice index across every policy domain. Taller bars (closer to 1) indicate strong within-party agreement on that issue; shorter bars flag areas where dissent is common.

### 3.4 Interpretation  
Without seeing the bars yet, we can anticipate:

- **Ideological fault lines.** Center-right and centrist groups may fracture on social or environmental votes, while left-wing factions split on internal market or security issues.  
- **Strategic dissent.** Sometimes individual MEPs cast protest votes to signal domestic constituencies or push leadership in coalition negotiations.  
- **Cross-national differences.** Even within a party group, national delegations may diverge when domestic politics or interest groups press them in opposite directions.

Once the bar charts are in place, we’ll explore which issues drive each group’s internal cohesion or discord.

---

## 4. Conclusions & Implications

By weaving together the Parliament-wide, policy-area, and within-party perspectives, this data story will show how institutional design, external events, and ideological cleavages jointly shape the EU’s legislative center of gravity—and where fault lines threaten to pull it apart. We’ll conclude with reflections on future challenges and the lessons roll-call data holds for collective decision-making in a diverse union.

