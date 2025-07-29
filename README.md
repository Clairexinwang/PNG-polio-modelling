## Summary at a Glance

- **Topic**: Polio vaccination modelling in fragile systems (Papua New Guinea)  
- **Approach**: SEIR model integrating key immunological processes (mucosal vs systemic immunity, waning, seroconversion delay)  
- **Platform**: Python (open-access code)  
- **Aim**: To inform equitable, real-world immunisation policy under operational constraints  
- **Relevance**: Global health strategy, outbreak control, health system evaluation  

## Immunologically Informed Modelling of Polio Vaccination Strategies to Mitigate cVDPV Risk in Papua New Guinea

This study seeks to develop an immunologically informed, policy-relevant transmission model to support vaccination strategies for poliovirus control in fragile health systems, using Papua New Guinea (PNG) as a case study. Amid resurging wild-type poliovirus and the recent emergence of circulating vaccine-derived poliovirus (cVDPV), PNG captures the complex interaction of biological uncertainty and operational constraints in the endgame stage of global polio eradication. Currently, modelling approaches often simplify immunological processes, however this risks policy decisions that are mathematically sound but not fully grounded in biological reality.

These observations prompted the development of this modelling framework that integrates core immunological mechanisms shaping virus persistence in low-coverage settings into a parsimonious SEIR model. Six empirically grounded vaccination scenarios, including OPV-only, IPV-only, phased rollouts, and delayed campaigns, will be simulated to assess different impacts on outbreak dynamics, immunity profiles, and cVDPV risk under varying constraints of coverage and timing. With the aim to generate policy-relevant insights that balance epidemiological effectiveness with implementation feasibility for immunisation policy in under-resourced settings, supporting global health agencies working at the intersection of immunisation strategy, disease control, and health systems strengthening. Beyond polio, the framework offers a replicable framework for modelling vaccination strategies against other pathogens in similarly vulnerable contexts, ensuring equity-driven public health decision-making.

## Research Leadership

This is an independent research project I undertook outside of my university coursework, motivated by my interest in applying epidemiological modelling to real-world challenges in global health and health system improvement. I developed the research question, designed the modelling framework, and identified the key areas that required investigation. However, I am grateful to several peers (Ollie, Farah, and Una) who supported the literature sourcing on topics such as the immunological context, modelling parameters and scenario justifications. While the design, direction, and development of the model were independently led, their assistance strengthened the background research and framing.

## Background and Rationale

Papua New Guinea (PNG) was chosen as it presents a relevant and timely context for modelling immunologically informed polio eradication strategies. Whilst officially declared free of wild poliovirus transmission in 2000, PNG has since experienced a resurgence of both wild-type and vaccine-derived poliovirus. A significant outbreak of circulating vaccine-derived poliovirus type 1 (cVDPV1) was confirmed in 2018 (Alleman et al., 2020), with new cases re-emerging in May 2025. Such occurrences reveal the fragility of progress in polio eradication when immunisation coverage and health system resilience are poorly sustained.

Globally, the burden of wild poliovirus has declined by over 99% since 1988, falling from an estimated 350,000 cases across more than 125 endemic countries to just six reported WPV1 cases in 2023, mainly from Afghanistan and Pakistan (World Health Organization, 2025). Observations from economic modelling suggests that global eradication could generate savings of between US$40–50 billion, concentrated mainly in low-income countries (Ochmann et al., 2017). However, the continued emergence of vaccine-derived polioviruses, now the only poliovirus strains circulating in the African Region, highlights the need for robust surveillance and tailored immunisation strategies (Polioeradication.org, 2024). Routine oral polio vaccine (OPV) coverage in PNG has remained below the 90% threshold required for population-level immunity, consistently shifting between 60–70%, declining further in more remote areas (Bauri, 2019) (Immunization Data, 2024). Supplementary immunisation activities (SIAs), though implemented across several years, have struggled to achieve consistent coverage levels (Vince et al., 2014). This coverage gap, combined with weak surveillance, cold-chain limitations, and persistent logistical barriers across mountainous and island regions, has resulted in large cohorts of children vulnerable to poliovirus transmission (Nations, 2023). In particular, vaccine-derived strains now pose a growing threat in areas where live-attenuated vaccines are used in cases of suboptimal uptake (Bauri, 2019).

While inactivated polio vaccine (IPV) has been added to national schedules in many countries to reduce the risk of type 2 re-emergence following the discontinuation of OPV2, it has a limited ability to induce mucosal immunity. As a result, whilst individuals may be protected from paralytic disease, nonetheless they may still be vulnerable to intestinal viral shedding and silent transmission. This immunological gap is particularly of concern in low-coverage settings where live-virus circulation can persist. The global rise in cVDPV outbreaks since 2016, including 1,048 cases in 2020 across 26 countries, many of which had previously been declared polio-free, raises important questions regarding the robustness of current risk mitigation strategies (Polioeradication.org, 2024). In response, this project specifically focuses on the immunological dynamics that drive such outbreaks: differences between mucosal and systemic immunity, waning protection over time, and variability in vaccine take, factors often simplified or excluded in existing models. PNG’s ongoing experience with cVDPV offers a real-world example in which the accuracy of immunologically detailed modelling can be evaluated against empirical outbreak data and field-level operational realities (Jglobalbiosecurity.com, 2025).

Moreover, PNG’s demographic profile, characterised by rapid population growth, high rurality (87% of the population living outside urban centres), and rising vaccine hesitancy, further complicates eradication efforts (Nations, 2023). A 2022 survey revealed that only 52% of respondents in PNG believed vaccines were safe, declining from 85% in 2015, reflecting wider trust and communication challenges in public health delivery (Bieb et al., 2017) (Harker, 2024). Within the same period, a notable decline in measles and DTP3 coverage were also observed, highlighting broader concerns around immunisation programme resilience (Immunization Data, 2024).

Finally, PNG represents a critical example for increasing the representation of low- and middle-income countries (LMICs) in global disease modelling. Health system fragility, environmental variability, and undernutrition, often prevalent in such contexts, can significantly shape vaccine performance, rollout feasibility, and population-level immunity. PNG thus offers not only a policy-relevant setting for polio control but also a methodologically rich environment for us to explore how biological mechanisms interact with fragile infrastructure, behavioural uncertainty, and delayed response systems. Insights generated from this study can help inform broader vaccine strategies across similar settings, contributing to global eradication goals while strengthening national preparedness and response capabilities.

---

## Objectives

1. To evaluate the epidemiological impact of oral polio vaccine (OPV)-only, inactivated polio vaccine (IPV)-only, and combined vaccination strategies in a low-resource setting with ongoing polio transmission, using Papua New Guinea as a case study.  
2. To incorporate key immunological mechanisms, including mucosal and systemic immunity, waning immunity, and vaccine take, into a mechanistically grounded SEIR transmission model.  
3. To simulate six evidence-defined vaccination scenarios, including delayed IPV rollout and waning immunity sensitivity, and assess their implications for outbreak dynamics, immunity profiles, and circulating vaccine-derived poliovirus (cVDPV) risk.  
4. To examine how vaccination timing, population coverage, and immune response dynamics interact under the operational constraints typical of fragile health systems.  
5. To generate context-specific, policy-relevant insights that can inform immunisation strategies for polio eradication, with an emphasis on feasibility, equity, and outbreak prevention in settings with limited resources.  
6. To demonstrate the transferability of biologically informed modelling frameworks to other vaccine-preventable diseases, contributing to improved vaccination planning across low- and middle-income countries.

## Contribution to Field

Whilst the usage of standard SEIR and SIRV frameworks for their interpretability and ease of alignment to available epidemiological data is recognised, they often rely on simplified representations of immunity, where vaccination is treated as a simple transition. These simplifications reduce the need for detailed immunological inputs, making such models more accessible for rapid policy use. However, I believe that this trade-off can limit the accuracy and relevance of projections, particularly in settings where immunisation systems are fragile and outbreak trajectories are shaped by gaps in immune protection. By embedding immunological mechanisms such as mucosal versus systemic immunity, waning protection, and vaccine take into the modelling framework, my aim is to produce insights that are not only technically robust but also grounded in biological and operational realism. I view this as a necessary step towards strengthening the credibility of model-informed vaccination strategies in vulnerable contexts, where the consequences of misinformed decisions can carry significant human and health system costs (Lai et al., 2022).

Thus, this project aims to addresses a critical and timely gap in both global health modelling and vaccine evaluation by integrating detailed immunological dynamics into forward simulations of OPV and IPV strategies, an approach that remains largely unexplored in fragile health system contexts, despite its potential to inform more effective policy. Using Papua New Guinea, a country facing resurging poliovirus and high cVDPV risk, as a case study grounds the work in urgent public health realities, whilst also allowing it to guide broader vaccination strategy design in other low-coverage, high-risk settings. In doing so, the project reflects core priorities in global health and health systems research: applying epidemiological insight to complex system challenges, and using rigorous, context-sensitive analysis to inform health system strengthening and evidence-based policy development.

By bridging theoretical modelling with the operational realities of fragile health systems, this research offers a scalable framework for translating complex dynamics into actionable insights for advancing efforts not only toward polio eradication but also broader infectious disease control.

---

## Methodology

When selecting a modelling framework, one of the most immediate concerns was the tendency of standard compartmental models, such as SIR or basic SEIR structures, to overlook critical immunological dynamics (CDC, 2025) (White, 2017). These frameworks often rely on assumptions of uniform vaccine uptake and lifelong immunity, which are poorly suited to settings like PNG, where oral polio vaccine (OPV) coverage varies highly, cold-chain logistics are fragile, and vaccine take varies considerably across subpopulations (Angelov et al., 2024) (Silal et al., 2022). Immunological distinctions, particularly between mucosal and systemic immunity, rates of waning protection, and heterogeneity in uptake, have demonstrated to significantly shape poliovirus transmission patterns (Sofonea, Cauchemez and Boëlle, 2022). Therefore, these dynamics have highlighted that they are far from being optional considerations, but rather they underpin the conditions under which circulating vaccine-derived poliovirus (cVDPV) resurges, as seen in PNG in both 2018 and 2025 (How modelling can better support public health policy making: the Lancet Commission on Strengthening the Use of Epidemiological Modelling of Emerging and Pandemic Infectious Diseases, 2023).

Whilst some modelling guidance advises incorporating such mechanisms only when supported by granular data, however the operational reality of PNG strongly justifies their inclusion (White, 2017) (Silal et al., 2022). Due to persistent gaps in OPV coverage, particularly in rural and remote areas, models that assume homogeneity in immune protection can substantially underestimate both vulnerability to infection and the potential for silent transmission. Furthermore, the model needed to remain parsimonious, tractable enough for parameter fitting and scenario testing, whilst still capturing the key biological processes (CDC, 2025) (Angelov et al., 2024).

To address this, an adapted SEIR structure was developed with targeted immunological extensions. This approach integrates key mechanisms, such as waning immunity, differential vaccine takes, and immune compartment transitions, while preserving analytical clarity and feasibility taking into consideration available data (Khalifi and Britton, 2022) (Sofonea, Cauchemez and Boëlle, 2022). It also reflects critiques of global dashboard-style models, which often apply overly generic assumptions and fail to capture contextual epidemiological variation. In contrast, this framework was intentionally designed for context-specific application, aligning with PNG’s distinctive demographic, immunological, and operational setting (Roberts et al., 2015).

The final model reflects a balance between theoretical robustness and real-world applicability, capable of producing credible, policy-informing insights even under conditions of ambiguity (How modelling can better support public health policy making: the Lancet Commission on Strengthening the Use of Epidemiological Modelling of Emerging and Pandemic Infectious Diseases, 2023). By embedding immunological realism where it is most crucial, the framework is better positioned to simulate cVDPV risk and guide immunisation strategy in fragile health systems (CDC, 2025) (White, 2017).

## Model Structure

The model will divide the population into compartments representing different epidemiological and immune dynamics, including:

- **S**: Susceptible  
- **E**: Exposed  
- **I**: Infectious  
- **Rm**: Recovered with mucosal immunity  
- **Rs**: Recovered with systemic immunity  
- **W**: Waned immunity  

## Parameters and Assumptions

All model parameters will be based on published estimates and validated sources such as WHO/UNICEF coverage data, GPEI outbreak records, and peer-reviewed studies.

- **Epidemiological parameters**:  
  - Basic reproduction number (R₀)  
  - Transmission rate (β)  
  - Recovery rate (γ)  

- **Vaccine-related parameters**:  
  - **VE₁**: Vaccine efficacy against infection  
  - **Ptake**: Probability of vaccine take  
  - **T**: Delay to seroconversion  
  - **VE₂**: Vaccine efficacy against transmission  
  - **Waning rate (w)**  
  - **Coverage (c)**  

- **Demographic parameters**:  
  - Birth rate  
  - Population size  
  - Vaccine rollout delay  

The model will assume a fixed population and no external importation of cases unless specified in sensitivity analyses.  
Immunisation access will initially be treated as uniform.

## Vaccination Strategies and Scenarios

The model will test six vaccination scenarios that reflect a mix of real-world policies and hypothetical alternatives:

1. **OPV-only (Baseline)**: Continued use of live-attenuated vaccines, commonly deployed in low-income settings but associated with cVDPV risk.  
2. **IPV-only**: A theoretical scenario focused on inactivated vaccine alone, assessing reduced transmission control but improved safety.  
3. **Mixed OPV-IPV Strategy**: Represents phased or combined rollout, simulating transition between vaccine platforms.  
4. **Delayed IPV Rollout**: Captures the impact of logistical and supply chain delays on population immunity and outbreak risk.  
5. **Waning Immunity Sensitivity**: Explores how different assumptions about the rate of waning protection affect long-term control.  
6. **High-Risk Scenario**: Based on PNG’s current context, with persistently low coverage and ongoing circulation of cVDPV.  

## Implementation

Simulations will be written in Python. All code and parameter tables will be openly shared on GitHub, alongside clear documentation to support reproducibility and potential collaboration.

## References

- Alleman, M.M., Jorba, J., Greene, S.A., Diop, O.M., Iber, J., Tallis, G., Goel, A., Wiesen, E., Wassilak, S.G.F. and Burns, C.C. (2020). *Update on vaccine-derived poliovirus outbreaks — worldwide, July 2019–February 2020*, MMWR. Morbidity and Mortality Weekly Report, 69(16), pp. 489–495. [doi](https://doi.org/10.15585/mmwr.mm6916a1)  
- Angelov, G., Kovacevic, R., Stilianakis, N.I. and Veliov, V.M. (2024). *An immuno-epidemiological model with waning immunity after infection or vaccination*. Journal of Mathematical Biology, 88(6). [doi](https://doi.org/10.1007/s00285-024-02090-z)  
- Bauri, M. (2019). *Notes from the field: Circulating vaccine-derived poliovirus type 1 and outbreak response — Papua New Guinea, 2018*. MMWR. Morbidity and Mortality Weekly Report, 68. [doi](https://doi.org/10.15585/mmwr.mm6805a6)  
- Bieb, S., Reza, S., Duncan, R., Hossain, M. and Clements, C.J. (2017). *A review of immunization services in Papua New Guinea, 2017*. [CAB Abstract](https://www.cabidigitallibrary.org/doi/pdf/10.5555/20193459426)  
- CDC (2025). *Technical Explainer: Infectious Disease Transmission Models*. [CDC](https://www.cdc.gov/cfa-modeling-and-forecasting/about/explainer-transmission-models.html)  
- Harker, R. (2024). *Childhood immunisation statistics*. [Parliament UK](https://researchbriefings.files.parliament.uk/documents/CBP-8556/CBP-8556.pdf)  
- *How modelling can better support public health policy making: The Lancet Commission on Strengthening the Use of Epidemiological Modelling of Emerging and Pandemic Infectious Diseases* (2023). The Lancet, 403(10429), pp. 789–791. [doi](https://doi.org/10.1016/s0140-6736(23)02758-7)  
- Immunization Data (2024). *WHO immunization data portal - detail page*. [WHO](https://immunizationdata.who.int/global/wiise-detail-page/measles-vaccination-coverage?CODE=PNG&ANTIGEN=&YEAR=)  
- Jglobalbiosecurity.com (2025). *View of disinfection measures and control of SARS-CoV-2 transmission*. [Jglobalbiosecurity](https://jglobalbiosecurity.com/index.php/up-j-gb/article/view/64/160)  
- Khalifi, M.E. and Britton, T. (2022). *Extending SIRS epidemics to allow for gradual waning of immunity*. [arXiv](https://arxiv.org/abs/2211.09062)  
- Nations, U. (2023). *Perception of the importance of vaccines for children declines in Papua New Guinea*. [UN](https://www.un.org/pt/information-center-pacific-unic/interview-dr-satish-gupta-dr-satish-gupta-chief-health-programme)  
- Ochmann, S., Roser, M., Dattani, S. and Spooner, F. (2017). *Polio*. [Our World in Data](https://ourworldindata.org/polio)  
- Polioeradication.org (2024). *GPEI - Vaccine derived poliovirus count*. [Polio Eradication](https://polioeradication.org/circulating-vaccine-derived-poliovirus-count/)  
- Silal, S., Bardsley, C., Menon, R., Abdullahi, L. and White, L. (2022). *Epidemiological modelling for public health decision making in sub-Saharan Africa: A strategic plan for capacity strengthening*. [OPML](https://www.opml.co.uk/files/Projects/a4964-epidem-modelling-capacity-strengthening.pdf?noredirect=1)  
- Sofonea, M.T., Cauchemez, S. and Boëlle, P.-Y. (2022). *Epidemic models: why and how to use them*. Anaesthesia Critical Care & Pain Medicine, 41(2), p.101048. [doi](https://doi.org/10.1016/j.accpm.2022.101048)  
- Roberts, M., Andreasen, V., Lloyd, A. and Pellis, L. (2015). *Nine challenges for deterministic epidemic models*. Epidemics, 10, pp.49–53. [doi](https://doi.org/10.1016/j.epidem.2014.09.006) 
- Vince, J.D., Datta, S.S., Toikilik, S. and Lagani, W. (2014). *Integrated package approach in delivering interventions during immunisation campaigns in a complex environment in Papua New Guinea: A case study*. Vaccine, 32(36), pp. 4614–4619. [doi](https://doi.org/10.1016/j.vaccine.2014.04.056)  
- White, P.J. (2017). *Mathematical Models in Infectious Disease Epidemiology*. Infectious Diseases, pp.49-53.e1. [doi](https://doi.org/10.1016/b978-0-7020-6285-8.00005-8)  
- World Health Organization (2025). *Poliomyelitis*. [WHO](https://www.who.int/news-room/fact-sheets/detail/poliomyelitis)  
