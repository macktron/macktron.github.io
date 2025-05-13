---
layout: custom_home

title: "Polarization in the European Parliament"

github_url: https://github.com/ByggeMandBob/your-repo
zip_url:     /downloads/archive.zip
tar_url:     /downloads/archive.tar.gz
---

---
In the last 20 years, political polarization has increased across Europe, reshaping democratic debate and trust in institutions. One key driver of this trend is the evolving media landscape. As traditional news sources lose dominance, fragmented platforms and social media algorithms increasingly amplify ideological divides.

A [2023 report by the European Commission](https://home-affairs.ec.europa.eu/whats-new/publications/media-and-polarisation-europe-strategies-local-practitioners-address-problematic-reporting-may-2023_en)🌐 highlights how polarization, particularly since the mid-2010s, has become a growing concern for democratic stability and local governance across EU member states.

To explore whether this broader societal polarization is mirrored in formal decision-making, we turn to the European Parliament, the EU’s central legislative body.

---

Data was obtained from **[VoteWatch Europe](https://www.votewatch.eu/)**🌐, which tracks how Members of the European Parliament (MEPs) vote on legislation. The dataset covers roll-call votes from 2005 to 2021. [Read more about dataset](/dataset/)📂. By analyzing these records over time, we aim to measure:
* How cohesion within eurpean parliment group evolves,
* How closely political groups align with each other,
* Within what policy areas divisions emerges,
* And whether there is a long-term trend toward greater fragmentation or cohesion.

---


# European Parliament Groups
Within the European Parliament, Members of the European Parliament (MEPs) are organized into transnational political groups called European Parliament Groups (EPGs). These groups bring together national parties from different EU countries that share similar political ideologies.

In our analysis, we focus on how these EPGs vote on different policy issues, as shifts in their voting patterns can reveal insights about change and polarization within the EU.


![MEP Table](images/epg_table_bokeh.png)

[See which policies European Parliament groups support most](/epgyesvotes/)📂.


![Polarization in the USA](images/polarization_USA.png)
*Rising ideological distance between parties is a global trend. Source: [Pew Research Center](https://www.pewresearch.org/politics/interactives/political-polarization-1994-2017)🌐.*

---

# Political polarization within EPGs


 Polarization is a fairly abstract concept but it can be quantified using the voting records of all Members of the European Parliament (MEPs)

A common metric for internal group agreement is the **Rice Index**, which produces a score between 0 and 1. This gives a simple, quantifiable measure of how unified a group is in its voting behavior. [Learn more about the Rice Index](/riceindex/)📂.



## Parliament-wide Agreement

<div style="display: flex; justify-content: center;">
  <iframe 
    src="/images/01_parliament_agreement.html"
    style="width: 90vw; max-width: 1000px; height: 600px; border: none;"
    loading="lazy">
  </iframe>
</div>

The graph shows the annual average Rice index for **all** roll-call votes. The x-axis runs from the earliest full year in our dataset to the most recent, and the y-axis show the Rice index illustrating the division between 0 (maximum division) and 1 (complete unity). 

### Interpretation of General Agreement 
Looking at the "spikes" and thus the periods with most disagreement the index exhibits two pronounced peaks over the 2005–2021 period both overlapping with systemic crises. In 2008 the index quickly rose from approximately 0.5 to 0.63, reflecting broad cross-group endorsement of emergency financial stability measures during the global banking collapse. Following this a gradual decline ensued a near 0.47 by 2019 driven by intensifying sovereign debt disputes and the polarization induced by the Brexit debate. [**BrexitPlorizing**](https://www.gisreportsonline.com/r/brexit-society-europe/)🌐

With the COVID-19 pandemic in early 2020, the Rice index rose again and climbed to 0.54 as MEPs unified around the €750 billion NextGenerationEU recovery fund, joint vaccine programs and health emergency protocols. [**EU**](https://commission.europa.eu/strategy-and-policy/recovery-plan-europe_en)🌐

In both instances the data indicate that extreme external shocks substantially increase legislative cohesion and in inter-crisis intervals, the ideological and national interest provoke disagreements.


## Polarization by Policy Area 🌐📈⚔️🌱

Examining voting patterns by individual policy area reveals the underlying ideological fault lines in Parliament and highlights the agrendas that produce the sharpest divisions. [Read a detailed explanation of each area](/policy_areas_explained/)📂


<div style="display: flex; justify-content: center;">
  <iframe 
    src="/images/agreement_by_policy_area_interactive.html"
    style="width: 90vw; max-width: 1000px; height: 650px; border: none;"
    loading="lazy">
  </iframe>
</div>

The interactive chart overlays the average line in black with colored lines for each policy area. Hovering over any point shows (Policy Area, Year, Rice). You can add or remove areas to compare their dynamics against the overall trend.


### Underlying Drivers  
Over time all policy area lines weave around an “average” curve thus there’s no single area that always leads or always lags. Instead different combinations become more consensual at different moments.

* **Persistent downward drift in overall cohesion.** 📉
  The “Average” line steadily slides from above-mid-range toward the lower half of the scale, indicating that outside crisis episodes, cross-party agreement has weakened over the last decade.

* **Legal Affairs leads volatility.** 👨🏻‍⚖️
  Of all ten areas the legal-affairs curve shows the greatest amplitude. It spikes to the top of the chart during emergency votes then falls sharply back toward the bottom in following years. This pattern with large spontaneous swings marks it as the most momentarily consensual but least stable area.

* **Consistent underperformance of social and environmental files.** 💔🌱
  The employment & social-affairs and environment & public-health lines spend significantly more time below the average than above. Their muted peaks and deeper troughs reflect ideological splits on labor and environmental regulation even when other areas diverge.

* **Mid-cycle leadership of culture & education and regional development.** 📚
  Outside of major crises the culture & education and regional development curves consistently lie above the average line, indicating that these files attract broader more stable majorities in routine legislative periods.

* **COVID-period surge in specific areas.** 🦠
  At the start of the pandemic the Rice index for culture & education, international trade and regional development all exhibit pronounced upward jumps and each rising well above the overall average. This reflects rapid cross-party alignment on recovery funding as mentioned before.

Apart from the two acute spikes triggered by systemic crises, roll-call cohesion in the European Parliament seem exhibited a gradual, long-term erosion as soon as soon as the crisis periods are over. Procedural areas, notably legal affairs, demonstrate pronounced volatility, while social and environmental areas remain staticly polarized.

In inter-crisis periods no single area consistently leads or lags. Each policy line oscillates around the declining average, reflecting how issue driven debates divides in the absence of a unifying emergency.


## Within-Party Cohesion
<div style="display: flex; justify-content: center;">
  <iframe 
    src="/images/02_within_party_agreement.html"
    style="width: 90vw; max-width: 1000px; height: 550px; border: none;"
    loading="lazy">
  </iframe>
</div>
 
The interactive line chart plots one line per political group, each initially visible but toggleable via checkboxes. It reveals which parties remain  unified across years and which show the greatest internal splits.

The Rice index of the internal European Parliament’s political groups reveal three clear dynamics:

**1. Enduring Mainstream Cohesion**
Center-right (EPP), social-democrat (S&D), liberal (REG/ALDE) and green (Greens/EFA) factions consistently occupy the upper portion of the scale. Greens/EFA exhibit the highest and most stable agreement while EPP, S&D and REG display moderate sensitivity to external stressors.

**2. Structural Fragmentation among Outliers**
Identity & Democracy (IDG) and non-attached members (NI) persistently record the lowest agreement levels. IDG’s index shows the internal split and loosely bound populist alliances. NI, lacking any formal grouping or shared platform, remains the most diverse with Rice values reaching as low as 0.27 after a decline up to 2014.

**3. Crisis-Induced Convergence**
Systemic shocks, most notably again the global financial crisis and the COVID-19 pandemic, temporarily elevate cohesion across nearly all groups. Even IDG registers its highest internal alignment during 2020 emergency votes, although it still remains below mainstream levels. Other groups exhibit only small or brief change in cohesion during crises showing their institutional resilience.

**Implications**
The data demonstrate that ideological compactness and formal group structures are the primary determinants of sustained voting agreement. Conversely, diverse coalitions fail to generate stable majorities except under extreme external pressure. In the absence of such shocks the less radical groups stay unified and are thus less prone to internal disagreement, both during crisis and stable periods. 

### Party Disagreement by Policy Area  
<div style="display: flex; justify-content: center;">
  <iframe 
    src="/images/04_bar_rice_by_policy_and_party.html"
    style="width: 90vw; max-width: 1000px; height: 800px; border: none;"
    loading="lazy">
  </iframe>
</div>

A dropdown-controlled bar chart 📊 shows for the selected party its average Rice index across every policy area. Taller bars (closer to 1) indicate strong internal party agreement on that issue.

Across the European Parliament’s political groups, voting cohesion clusters around each faction’s defining priorities. Greens/EFA ☘️ record near unity on environment & public health, employment & social affairs and gender equality which reflects their integrated Green Deal agenda, while S&D remain most cohesive on gender equality, development, budgetary control and culture & education in line with their social democratic platform 🎓. Renew Europe shows moderate agreement on innovation and rights focused areas particularly culture & education and development, but it fractures on international trade🏗️. The Left peaks on gender equality and development but divides sharply on agriculture and trade. EPP maintains strong discipline in justice-related areas (culture & education, legal affairs) but reveals tension in agriculture and environmental votes👨🏻‍⚖️. At the extremes Identity & Democracy and non attached members exhibit consistent low agreement across all domains, showing the role of ideological compactness and formal group structures in sustaining legislative unity📉.

Together, these patterns confirm that **ideological compactness** and **institutional cohesion** are the principal drivers of stable voting unity. Formal groups with clear, shared agendas (Greens/EFA, S&D, EPP) achieve higher, more consistent Rice indices in areas central to their identity, while loose coalitions or individuals outside recognized groups struggle to agree on any policy area.


[Read the full analysis here](/policy_areas/)📂


![A lighter moment](images/original.png)
*The Atlantic; Getty. [Source](https://www.theatlantic.com/ideas/archive/2022/05/us-democrat-republican-partisan-polarization/629925/)*🌐

---

# Political Polarization Between European Parliamentary Groups 

Understanding the similarity in voting behavior between different EPGs requires more than conventional measures. [The Rice Index](/riceindex/)📂, commonly used to quantify intra-group cohesion, is limited in this context since it evaluates agreement within a single group, but does not account for variations in group size or the frequency of abstentions.

## Measuring Inter-Group Similarity

To overcome these limitations, a [custom agreement index](/customindex/)📂 is applied. This metric compares how two groups distribute their votes across the categories Yes✅, No🛑, and Abstain🤷🏻‍♂️. It adjusts for differences in group size and calculates the degree of similarity in their voting patterns. The result is a value between 0 and 1, where 1 indicates identical behavior across votes.
[Learn more about the Custom Index](/customindex/)📂

## Visualizing Voting Alignment ⚖️

Based on the calculated similarities, clustering is constructed in which each EPG is mapped as a point in space. Groups with similar voting patterns are positioned closer together🫱🏻‍🫲🏾, while those with more divergent behavior are farther apart💔. [Learn more about the clustering](/pca/)📂



<div style="display: flex; justify-content: center; margin: 0; padding: 0; line-height: 0;">
  <iframe 
    src="/images/epg_clustering_combined.html"
    style="width: 90vw; max-width: 1000px; height: 700px; border: none; display: block; margin: 0; padding: 0;"
    loading="lazy">
  </iframe>
</div>


Even though the EPGs shift position from year to year trends between parties can still be observed.

* The **Greens/EFA** and **The Left** are often located close to each other in the similarity maps, which means they tend to vote in similar ways.
* The same goes for **S&D** and **Renew Europe**.
* On the other hand, the **IDG** is usually far from the other groups. This shows they vote very differently, which fits with their position as a right-wing, nationalist group.
* **Non-attached members** (NI) also tend to be far from the rest. These members don’t belong to any formal political group and often represent very different or unique national parties, so their voting behavior is harder to group.
* From 2005 to 2019, the positions of most groups remain steady. But starting in 2020, we see groups beginning to spread apart more. In particular, **IDG** and **EPP** move away from each other. **REG** also shifts away from the center. This shift happens around the time of the **COVID-19 pandemic**, which brought many new laws and decisions. The differences in how groups responded, for example on lockdowns, vaccine strategies, or EU-wide recovery plans, [likely made these divisions stronger](https://ecfr.eu/publication/europes-invisible-divides/)🌐.


The following table summarizes the most and least similar EPG pairings annually🗓️:

| Year Range     | Most Similar EPGs     | Least Similar EPGs    |
|----------------|------------------------|------------------------|
| 2005–2007      | Greens/EFA – The Left | IDG – The Left         |
| 2008–2010      | Greens/EFA – REG      | IDG – The Left         |
| 2011–2012      | REG – S&D             | IDG – The Left         |
| 2013–2014      | Greens/EFA – S&D      | IDG – The Left         |
| 2015           | REG – S&D             | IDG – REG              |
| 2016           | Greens/EFA – S&D      | IDG – REG              |
| 2017–2019      | Greens/EFA – The Left | EPP – IDG              |
| 2020           | Greens/EFA – The Left | IDG – The Left         |
| 2021           | Greens/EFA – The Left | EPP – IDG              |
| 2022           | Greens/EFA – S&D      | IDG – The Left         |



## How Similar European Parliament Groups Voted Over Time Across Policy Areas

The PCA clustering process is applied using the same custom agreement index as in the general analysis, but performed separately for each policy area. This allows for the examination of voting alignment and polarization within specific domains of legislation.


<div style="display: flex; justify-content: center;">
  <iframe 
    src="/images/epg_clustering_per_policy_area.html"
    style="width: 90vw; max-width: 1000px; height: 700px; border: none;"
    loading="lazy">
  </iframe>
</div>



* In **budgetary control**, a clear realignment appears in 2012, during the peak of the **Eurozone debt crisis**. The **EPP (centre-right)** and **Greens/EFA (green-left)**, who previously showed some alignment, start to diverge sharply. This coincides with increasing disagreements over fiscal discipline, austerity, and EU-level spending. The crisis pushed parties into more ideologically defined stances. [Read more on the Euro crisis](https://www.investopedia.com/terms/e/european-sovereign-debt-crisis.asp/)🌐. By 2013, **REG** starts to shift positions in this area, moving away from its previous closeness with **S&D** and closer to **EPP** on certain budget votes. This could reflect its liberal economic stance becoming more pronounced during recovery debates.

* In the area of **environment and public health**, we see strong, consistent clustering between **Greens/EFA**, **The Left**, and **S&D**, especially in years like 2018. Their alignment reflects shared support for EU-led climate policy, regulation, and health measures.

* In 2020, a major divergence emerges between **EPP** and **IDG** across multiple policy areas. COVID-19 debates — on vaccines, lockdowns, recovery funds, and public health — force parties to take clear stances. IDG often resisted joint EU responses, while EPP leaned toward centralized action, leading to increased separation in voting similarity.


Crises and high-stakes policy moments, like the Eurozone crisis (2012) or the COVID-19 pandemic (2020), act as catalysts for polarization in voting patterns of the European Parliament. These shifts are not uniform across all policy areas. In economic and budgetary matters, we often see movement between liberal and conservative blocs. In climate and health, the fault line is clearer: pro-EU integration vs. nationalist opposition.

Some votes show up as especially divergent or unified between specific groups. [Find out more about the most distinct simmilarities between EPGs over years and policy areas](/distinctsimilarities/)📂



# Final Thoughts 

In sum, the analysis reveals a European Parliament that responds predictably to external shocks. During crises such as the global financial meltdown and the COVID-19 emergency, MEPs unite across ideological lines to pass landmark measures, driving temporary spikes in the Rice Index and drawing disparate groups into closer voting alignment. Yet in the mid-crisis times overall cohesion erodes, procedural areas like legal affairs oscillate wildly, and social and environmental areas remain stubbornly divided.

At the party level, formal structures and shared platforms enforce sustained unity. Mainstream factions like EPP, S&D, Renew Europe and Greens/EFA—consistently rank highest in internal agreement, while populist outliers (IDG) and non-attached MEPs are consistently agreeing a very little. Crisis-induced voting induce even for these loose coalitions a momentary alignment, but once the emergency recedes, they slip back into deep internal splits.

Intergroup similarity further shows Europe’s fault lines. Greens/EFA and The Left often vote in similar, as do S&D and Renew Europe, while IDG and non-attached members remain diverged from other groups. Clustering by policy area shows where lines of heated disagreement run deepest. Budgetary control cleaves liberal and conservative camps during fiscal crises, climate and health unite the pro-integration blocs, and agricultural and trade areas fracture the moderate middle.

Together, these dynamics tells the story of an institution both resilient and strained. The European Parliament can find unity when necessity demands but in the more routine rhythm of legislation, the strong forces of ideology, national interest and institutional design forces disagreements. One might find it reassuring to see a higher level of collaboration during crisis, but how long do we have to wait for the next pandemic to unite us...?🦠🟰🫱🏻‍🫲🏾
