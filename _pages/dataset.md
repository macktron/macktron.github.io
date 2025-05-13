---
layout: blank
title: Dataset
permalink: /dataset/
---

The dataset used in this project is sourced from **[VoteWatch Europe](https://www.votewatch.eu/)**, an independent organization that tracks voting behavior in the European Parliament. It captures how Members of the European Parliament (MEPs) voted::  **in favor**, **against**, or **abstained**—on legislative proposals. Alongside each vote, it includes rich metadata about the individual MEP and the vote context.

This allows for a detailed examination of voting patterns across countries, political groups, and time periods, offering insights into trends of polarization, party cohesion, and ideological shifts.

---

### 🗃️ Cleaned Dataset Structure

The cleaned dataset contains the following variables:

- **full_name**: Full name of the MEP  
- **country**: Member state's name  
- **national_party**: The national political party of the MEP  
- **epg**: European Parliamentary Group affiliation  
- **mep_id**: Unique identifier for each MEP  
- **vote_code**: Categorical code for vote type (e.g., for, against, abstain)  
- **vote**: Human-readable vote label  
- **date**: Date of the vote  
- **title**: Title of the legislative proposal  
- **policy_area**: Thematic category (e.g., environment, economy)  
- **ep_session**: European Parliament session identifier  
- **year**: Year of the vote  
- **month**: Month of the vote  

---

This dataset spans votes from **2005 to 2021**, covering multiple parliamentary terms and allowing us to observe long-term shifts and emerging patterns in the legislative alignment of MEPs.

You can explore how voting behavior varies across **time**, **countries**, **policy areas**, and **political groups** in the visualizations provided throughout the site.
