# Immunologically Informed Modelling of Polio Vaccination Strategies to Mitigate cVDPV Risk in Papua New Guinea

This project aims to develop an immunologically grounded, policy-relevant transmission model to inform vaccination strategies for poliovirus control in fragile health systems, using Papua New Guinea (PNG) as a case study. Amid resurging wild-type poliovirus and the documented emergence of circulating vaccine-derived poliovirus (cVDPV), PNG exemplifies the complex intersection of biological uncertainty and operational constraint in the endgame stage of global polio eradication. Current modelling approaches often simplify immunological processes, risking policy decisions that are mathematically sound but biologically incomplete.

To address this, the project integrates mucosal versus systemic immunity, waning, and vaccine take into a parsimonious SEIR model. Six empirically grounded vaccination scenarios, including OPV-only, IPV-only, phased rollouts, and delayed campaigns, will be simulated to assess differential impacts on outbreak dynamics, immunity profiles, and cVDPV risk under varying constraints of coverage and timing.

The aim is to generate policy-relevant insights that balance epidemiological effectiveness with implementation feasibility for immunisation policy in under-resourced settings, supporting global health agencies working at the intersection of immunisation strategy, disease control, and health systems strengthening. Beyond polio, the framework offers a replicable architecture for modelling vaccination strategies against other pathogens in similarly vulnerable contexts, ensuring equity-driven public health decision-making.

---

## Background and Rationale

Papua New Guinea (PNG) presents a relevant and timely context for modelling immunologically informed polio eradication strategies. Although certified free of wild poliovirus in 2000, PNG has since experienced a resurgence of both wild-type and vaccine-derived poliovirus. A significant outbreak of circulating vaccine-derived poliovirus type 1 (cVDPV1) was confirmed in 2018, with new cases re-emerging in May 2025. These developments demonstrate the fragility of progress in polio eradication when immunisation coverage and health system resilience are insufficiently maintained (Valentine et al., 2020; CDC, 2019).

Routine oral polio vaccine (OPV) coverage in PNG has remained below the 90% threshold required for population-level immunity, consistently shifting between 60–70% and falling further in more remote areas (CDC, 2014; WHO/UNICEF, 2023). Supplementary immunisation activities (SIAs), whilst carried out in multiple years, have not consistently achieved the desired reach (Vince et al., 2014; Datta et al., 2014). This coverage gap, combined with weak surveillance, cold-chain limitations, and persistent logistical barriers across mountainous and island regions, has resulted in large cohorts of children vulnerable to poliovirus transmission (UNIC Pacific, 2023). In particular, vaccine-derived strains now pose a growing threat in areas where live-attenuated vaccines are used in the context of suboptimal uptake (Datta et al., 2014).

This project focuses specifically on the immunological dynamics that drive such outbreaks, differences between mucosal and systemic immunity, waning protection over time, and variability in vaccine take — factors often simplified or excluded in existing models. PNG’s ongoing experience with cVDPV offers a real-world test case in which the accuracy of immunologically detailed modelling can be evaluated against empirical outbreak data and field-level operational realities (Valentine et al., 2020).

Moreover, PNG’s demographic profile — characterised by rapid population growth, high rurality (87% of the population living outside urban centres), and rising vaccine hesitancy — further complicates eradication efforts (UNIC Pacific, 2023). A 2022 survey reported that only 52% of respondents in PNG believed vaccines were safe, which has dropped sharply from 85% in 2015, reflecting wider trust and communication challenges in public health delivery (Informit, 2023; Parliament UK, 2019). Within the same period, a notable decline in measles and DTP3 coverage was observed, highlighting broader concerns around immunisation programme resilience (WHO/UNICEF, 2023).

For these reasons, PNG offers not only a policy-critical setting for polio control but also a methodologically rich environment for modelling. It allows us to explore how biological mechanisms interact with fragile infrastructure, behavioural uncertainty, and delayed response systems — realities that mirror conditions in many other low- and middle-income countries (LMICs). Insights generated from this study could help inform broader vaccine strategies across similar settings, contributing to global eradication goals while strengthening national preparedness and response capabilities.

---

## Objectives

1. To evaluate the epidemiological impact of oral polio vaccine (OPV)-only, inactivated polio vaccine (IPV)-only, and combined vaccination strategies in a low-resource setting with ongoing polio transmission, using Papua New Guinea as a case study.
2. To incorporate key immunological mechanisms, including mucosal and systemic immunity, waning immunity, and vaccine take, into a mechanistically grounded SEIR transmission model.
3. To simulate six evidence-defined vaccination scenarios, including delayed IPV rollout and waning immunity sensitivity, and assess their implications for outbreak dynamics, immunity profiles, and circulating vaccine-derived poliovirus (cVDPV) risk.
4. To examine how vaccination timing, population coverage, and immune response dynamics interact under the operational constraints typical of fragile health systems.
5. To generate context-specific, policy-relevant insights that can inform immunisation strategies for polio eradication, with an emphasis on feasibility, equity, and outbreak prevention in settings with limited resources.
6. To demonstrate the transferability of biologically informed modelling frameworks to other vaccine-preventable diseases, contributing to improved vaccination planning across low- and middle-income countries.

---
### Significance

This project addresses a critical and timely gap in both global health modelling and vaccine policy evaluation by integrating detailed immunological dynamics into forward simulations of OPV and IPV strategies — something that has rarely been done in fragile health system contexts. Existing models often prioritise mathematical simplicity over biological accuracy, overlooking key processes like mucosal versus systemic immunity, waning protection, and vaccine take.

My approach challenges that norm by embedding these immunological realities into a policy-relevant framework, enabling more precise assessment of outbreak risks under diverse vaccination scenarios. Using Papua New Guinea, a country facing resurging poliovirus and high cVDPV risk, as a case study grounds the work in urgent public health realities, whilst also allowing it to guide broader vaccination strategy design in other low-coverage, high-risk settings.

In doing so, the project reflects core priorities in global health and health systems research: applying epidemiological insight to complex system challenges, and using rigorous, context-sensitive analysis to inform health system strengthening and evidence-based policy development.

By bridging theoretical modelling with the operational realities of fragile health systems, this research offers a scalable framework for translating complex dynamics into actionable insights for advancing efforts not only toward polio eradication but also broader infectious disease control.

---

## Methodology

This project aims to develop a compartmental SEIR (Susceptible–Exposed–Infectious–Recovered) transmission model tailored to reflect the specific immunological and operational realities of poliovirus control in Papua New Guinea (PNG). The model is designed to go beyond traditional structures by integrating immunological mechanisms that are often oversimplified in standard frameworks, including mucosal versus systemic immunity, waning protection, and variability in vaccine take following OPV and IPV administration.

### Model Structure

The model will divide the population into compartments representing different epidemiological and immune states, including:
- **S**: Susceptible  
- **E**: Exposed  
- **I**: Infectious  
- **Rm**: Recovered with mucosal immunity  
- **Rs**: Recovered with systemic immunity  
- **W**: Waned immunity

### Parameters and Assumptions

All model parameters will be based on published estimates and validated sources such as WHO/UNICEF coverage data, GPEI outbreak records, and peer-reviewed studies.

- **Epidemiological parameters**: Basic reproduction number (R₀), Transmission rate (β), Recovery rate (γ)  
- **Vaccine-related parameters**:  
  - VE₁: Vaccine efficacy against infection  
  - P<sub>take</sub>: Probability of vaccine take  
  - T: Delay to seroconversion  
  - VE₂: Vaccine efficacy against transmission  
  - Waning rate (w)  
  - Coverage (c)  
- **Demographic parameters**: Birth rate, Population size, Vaccine rollout delay

The model will assume a fixed population and no external importation of cases unless specified in sensitivity analyses. Immunisation access will initially be treated as uniform.

---

## Vaccination Strategies and Scenarios

The model will test six vaccination scenarios that reflect a mix of real-world policies and hypothetical alternatives:

1. **OPV-only (Baseline):** Continued use of live-attenuated vaccines, commonly deployed in low-income settings but associated with cVDPV risk.  
2. **IPV-only:** A theoretical scenario focused on inactivated vaccine alone, assessing reduced transmission control but improved safety.  
3. **Mixed OPV-IPV Strategy:** Represents phased or combined rollout, simulating transition between vaccine platforms.  
4. **Delayed IPV Rollout:** Captures the impact of logistical and supply chain delays on population immunity and outbreak risk.  
5. **Waning Immunity Sensitivity:** Explores how different assumptions about the rate of waning protection affect long-term control.  
6. **High-Risk Scenario:** Based on PNG’s current context, with persistently low coverage and ongoing circulation of cVDPV.

---

## Implementation

Simulations will be written in **R** or **Python**. All code and parameter tables will be openly shared on GitHub, alongside clear documentation to support reproducibility and potential collaboration.

---

## References

- Centers for Disease Control and Prevention (CDC), 2014. *Progress toward poliomyelitis eradication—Papua New Guinea, 1996–2012*. *MMWR. Morbidity and Mortality Weekly Report*, 63(17), pp.369–373.
- Centers for Disease Control and Prevention (CDC), 2019. *Update on vaccine-derived poliovirus outbreaks — worldwide, July 2018–February 2019*. *MMWR. Morbidity and Mortality Weekly Report*, 68(5), pp.225–230.
- Datta, S.S., Vince, J.D., Toikilik, S. and Lagani, W., 2014. Integrated package approach in delivering interventions during immunisation campaigns in a complex environment in Papua New Guinea: a case study. *Vaccine*, 32(28), pp.3551–3555. https://doi.org/10.1016/j.vaccine.2014.04.056.
- Informit, 2023. *Papua New Guinea: A vaccine hesitancy hotspot*. [online] Available at: https://search.informit.org/doi/abs/10.3316/INFORMIT.759019788553702 [Accessed 26 Jul. 2025].
- House of Commons, 2019. *Falling vaccination rates in developing countries*. Briefing Paper CBP-8556. [online] Available at: https://researchbriefings.files.parliament.uk/documents/CBP-8556/CBP-8556.pdf [Accessed 26 Jul. 2025].
- United Nations Pacific, 2023. *Interview with Dr. Satish Gupta: Immunisation challenges in PNG*. [online] Available at: https://www.un.org/pt/information-center-pacific-unic/interview-dr-satish-gupta [Accessed 26 Jul. 2025].
- Valentine, N., Thomas, J. and Isahak, L., 2020. The 2018 outbreak of vaccine-derived poliovirus in Papua New Guinea. *Journal of Global Biosecurity*, 2(1). [online] Available at: https://doi.org/10.31646/gbio.64 [Accessed 26 Jul. 2025].
- World Health Organization (WHO)/UNICEF, 2023. *Measles vaccination coverage: Papua New Guinea*. [online] Available at: https://immunizationdata.who.int/global/wiise-detail-page/measles-vaccination-coverage?CODE=PNG [Accessed 26 Jul. 2025].







