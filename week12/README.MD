
# REPORT — Environmental Impacts of Data Centres & Digital Platforms

> **Instructions**: Work in **pairs**. Use this template to write your 2–3 page Markdown report. Replace all prompts with your content and delete helper text.

First, choose:
- **One data‑centre operator** (e.g., AWS, Azure/Microsoft, Google, Equinix, Digital Realty, OVH) and
- **One digital platform** (e.g., YouTube, Instagram, Netflix, TikTok, X, or a generative‑AI service).

> Keep claims grounded in the companies’ published reports or reputable analyses. **Link and cite every number.**


## 1) Executive summary (≈150 words)
*Give one‑sentence findings for (a) the data‑centre operator or (b) the digital platform. State the single most impactful improvement you recommend to each, with one reason why it would help.*
This report evaluates Microsoft Azure as a data-centre operator and Netflix as a digital platform, focusing on energy use, carbon emissions, and water impacts. Microsoft has made significant progress toward its 2030 sustainability goals by reducing operational emissions, expanding renewable-energy procurement, and investing in water-positive initiatives. However, rapid growth in AI and cloud infrastructure continues to increase supply-chain (Scope 3) emissions [1]. Netflix has committed to reducing emissions by approximately 50% by 2030 and has already reduced its Scope 1 and Scope 2 emissions by half compared with 2022 levels [5]. The most impactful improvement for Microsoft would be publishing region-level location-based (LB) emissions and water-use data, allowing customers to make more carbon-aware deployment decisions. For Netflix, the most effective improvement would be adopting default carbon-aware scheduling for non-urgent analytics and background processing workloads. This would reduce emissions associated with cloud computing without affecting the viewing experience of subscribers.

## 2) Case A — Data‑centre operator: <Operator name>

### 2.1 What they report (energy, carbon by scope, water)
*Bullet the most recent **quantitative** facts the operator discloses. Include any notes on Scope 1/2/3, renewable/clean‑power strategy, and **water** (e.g., WUE or water‑reduction initiatives). Each item should end with an inline citation link.*
Microsoft aims to become carbon negative, water positive, and zero waste by 2030 [1].
Microsoft reduced Scope 1 and Scope 2 emissions by 29.9% relative to its 2020 baseline, although Scope 3 emissions increased because of growth in cloud and AI infrastructure [4].
Microsoft has contracted approximately 34 GW of renewable and carbon-free electricity across 24 countries [1].
In FY2024, Microsoft contracted nearly 21.9 million metric tonnes of carbon removals to support its carbon-negative target [1].
Microsoft reports that direct-to-chip cooling technology can save more than 125 million litres of water per facility each year compared with traditional cooling approaches [1].
Microsoft's contracted water replenishment volume increased to approximately 50 million cubic metres in FY2024, up from 25.5 million cubic metres in FY2023 [2].
In Quincy, Washington, Microsoft partnered with local authorities on a water reuse project that reduced potable water consumption by 97% and returned approximately 1.5 million cubic metres of water annually to the local community [3].

- Example: "Scope 2 (location‑based) trend in region X …" (source)
- Example: "Water reporting / WUE (if published) …" (source)

### 2.2 LB vs MB in practice (2–4 sentences)
*Explain the difference between **location‑based (LB)** and **market‑based (MB)** emissions for electricity, and why LB is the right view for **engineering choices** (region/time). If available, add one sentence referencing your operator’s cloud carbon tooling (e.g., AWS CCFT, Google Carbon Footprint, Azure Carbon Optimisation) and what it shows.*
Location-based (LB) emissions reflect the actual carbon intensity of the electricity grid supplying a facility. Market-based (MB) emissions account for contractual purchases such as renewable-energy certificates and power-purchase agreements. MB accounting is useful for corporate reporting because it reflects procurement choices, while LB emissions show the real-world impact of where and when electricity is consumed. For engineering decisions such as workload placement, region selection, and scheduling, LB emissions are more useful because they reveal differences between electricity grids. Microsoft provides sustainability and carbon-management tools through Azure that help organisations evaluate the environmental impact of cloud workloads and improve deployment decisions [1].

### 2.3 Risks & trade‑offs (grid & water) (≈1 paragraph)
*Discuss siting/latency vs. carbon trade‑offs and **water** considerations (evaporative vs air/refrigerant cooling; potential **peak‑day water spikes**). Cite at least **two** sources here.*
Data-centre operators face a trade-off between locating facilities close to users for lower latency and locating them in regions with cleaner electricity grids. A region with low-carbon electricity may be geographically distant from users, potentially increasing latency or network costs. Water is another major consideration. Evaporative cooling can improve energy efficiency but may require large quantities of water during hot periods. Alternative cooling approaches such as direct-to-chip or refrigerant-based systems reduce water consumption but can increase infrastructure complexity and capital costs. As AI workloads grow, peak-day water demand may place additional stress on local water supplies, particularly in water-stressed regions. Microsoft has responded by investing in water replenishment projects and developing cooling systems that significantly reduce water use [1][2][3].

## 3) Case B — Digital platform: <Platform name>

### 3.1 What’s public (policies, metrics)
*Summarise what the platform or its parent company reports about energy/carbon (by scope where applicable) and any relevant targets or initiatives. Use concrete numbers where possible and cite.*
Netflix has committed to reducing its emissions by approximately 50% by 2030 and matching remaining emissions through investments in natural climate solutions from 2022 onward [5][6]. The company reports that it is on track to meet these goals and follows an "Optimize, Electrify, Decarbonize" (OED) framework for emissions reduction [5]. According to Netflix's 2024 sustainability update, Scope 1 and Scope 2 emissions were reduced by approximately 50% compared with 2022 levels [5]. Netflix states that most emissions originate from production activities, corporate operations, and its broader value chain rather than from streaming itself [5].
### 3.2 Operational realities & carbon‑aware opportunities (≈1 paragraph)

*Identify the dominant workloads (e.g., video streaming vs. AI inference) and describe **one** realistic way to reduce LB emissions **without harming user experience** (e.g., time‑shifting non‑urgent batch work, region choice for background analytics, demand‑shaping during dirty hours). Cite at least one supporting source.*
Netflix's dominant workload is large-scale video streaming, supported by content delivery networks, cloud infrastructure, analytics platforms, and recommendation systems. Because streaming must occur when users request content, much of the workload cannot be shifted in time. However, background activities such as analytics processing, machine-learning model training, content indexing, and reporting tasks can be scheduled during periods when electricity grids are cleaner. Carbon-aware scheduling can reduce location-based emissions without affecting user experience because these workloads are not latency-sensitive. Microsoft and other cloud providers increasingly support sustainability monitoring tools that can help identify lower-carbon execution windows and regions [1].

### 3.3 Water awareness (3–5 sentences)
*If the platform operates first‑party data centres (or relies heavily on hyperscalers in water‑stressed regions), note potential WUE/peak‑day implications. If no data is available, state that and explain what should be reported.*
Netflix does not operate hyperscale data-centre infrastructure at the scale of major cloud providers and relies heavily on external cloud and networking partners. Consequently, detailed water-use metrics related to streaming infrastructure are not publicly disclosed by Netflix. Nevertheless, the cloud providers supporting Netflix's services consume substantial quantities of water for cooling. As AI and digital services expand, stakeholders would benefit from more detailed reporting on indirect water impacts, including regional water-use effectiveness (WUE), water-stress exposure, and peak-day consumption associated with outsourced cloud services. Greater transparency would improve understanding of the platform's full environmental footprint.



## 4) Two concrete recommendations (≈150–200 words total)
- **For the operator**: *Write 2–4 sentences. Make it specific, feasible this year (e.g., expand region‑level LB transparency; heat‑reuse; publish WUE and peak‑day capacity; carbon‑aware job slots).*  
- **For the platform**: *Write 2–4 sentences. Example themes: default carbon‑aware scheduling for non‑urgent tasks; nudge background jobs to low‑carbon regions; lightweight formats/bitrates at no QoE loss; publish more granular impact data.*

For Microsoft Azure

Microsoft should publish region-level location-based emissions data and detailed water metrics, including water-use effectiveness (WUE) and peak-day water capacity for every major Azure region. This would enable customers to choose deployment locations based on actual environmental impact rather than annual averages. Microsoft should also expand carbon-aware workload scheduling options within Azure so that batch workloads can automatically run when electricity grids are cleaner.

For Netflix

Netflix should implement default carbon-aware scheduling for non-urgent analytics, machine-learning training, reporting, and content-processing workloads. These tasks can often be shifted to times or regions with lower-carbon electricity without affecting viewers. Netflix should also publish more detailed information about the environmental impact of its cloud infrastructure, including indirect water consumption and cloud-region emissions, to improve transparency and accountability.

## References (numbered list with links)
*List every source you cited, as a numbered list. Use direct links to official reports or reputable analyses. Example:*  
1. *Organisation/Report title (Year).* [Link](https://example.org)  
2. *Provider tool or dashboard doc.* [Link](https://example.org)
[1] Microsoft Environmental Sustainability Report 2025. https://www.microsoft.com/en-us/corporate-responsibility/sustainability/report/

[2] Microsoft Sustainability Report – Water Replenishment Progress. https://www.microsoft.com/en-us/corporate-responsibility/sustainability/report/

[3] Microsoft Water Reuse Project, Quincy, Washington. https://www.microsoft.com/en-us/corporate-responsibility/sustainability/report/

[4] Microsoft Environmental Sustainability Report Summary (FY2024). https://www.sustainabilityreports.com/microsoft/2025/environmental-sustainability-report

[5] Netflix Sustainability Progress: Three Years In (2024). https://about.netflix.com/en/news/netflix-sustainability-progress-three-years-in

[6] Netflix Sustainability Overview. https://about.netflix.com/sustainability

> **Tips**: Prefer recent operator/platform sustainability reports; electricity‑sector analyses (e.g., IEA/EIA); major cloud carbon‑tool docs (AWS CCFT / Google Carbon Footprint / Azure Carbon Optimisation). Match each number to an inline citation in the text like this: `[1]`.

---

## Optional appendix (delete if unused)
- **Figure A1**: *Intensity vs time for two regions with your recommended window highlighted.*
- **Data extraction notes**: *Where you pulled numbers from (page/table), any assumptions.*
- **Glossary (one‑liners)**: *LB, MB, WUE, Scope 1/2/3.*

---

### Formatting hints (delete after drafting)
- Use short paragraphs, bullets, and tables sparingly for clarity.
- Keep units consistent (e.g., gCO₂/kWh; kgCO₂). If you compute anything, show the formula.
- Prefer **location‑based** data for comparisons across regions/times; mention MB only to explain the accounting difference.
- Avoid vague claims (e.g., “green”, “sustainable”) unless backed by a specific metric and citation.
