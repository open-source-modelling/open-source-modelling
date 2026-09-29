## Open-Source Modelling

**Open, tested algorithms for actuaries and risk managers**, as an alternative to closed commercial software.

Everything here is free to use and fork under the MIT licence (the asset-liability model uses MPL-2.0). Each algorithm comes with its source paper or regulatory document, a worked example and tests, so you can check the result instead of trusting it.

Open-Source Modelling started in Milan in 2021. It is funded and maintained by [Qnity Consultants](https://qnityconsultants.com).

---

### Start here

| Repository | What it is |
|---|---|
| [insurance_python](https://github.com/open-source-modelling/insurance_python) | Every Python algorithm in one place: yield curves, short-rate models, bootstrapping, time series |
| [Open_Source_Economic_Model](https://github.com/open-source-modelling/Open_Source_Economic_Model) | A full asset-liability model (OSEM) for insurers and pension funds, with a methodology document |
| [insurance_matlab](https://github.com/open-source-modelling/insurance_matlab) | The same algorithms for Matlab users |
| [insurance_jupyter](https://github.com/open-source-modelling/insurance_jupyter) | Notebooks that walk through the methods step by step |
| [insurance_skills](https://github.com/open-source-modelling/insurance_skills) | AI assistant skills for actuarial work, where the calculation runs in Python and the assistant is just the interface |

### What's covered

**Yield curves and Solvency II**
- Smith-Wilson interpolation and extrapolation, following EIOPA's technical documentation, with calibration of alpha
- Nelson-Siegel-Svensson curve fitting
- Checks that recalculate EIOPA's monthly risk-free rate curves
- [Every historical EIOPA curve](https://github.com/open-source-modelling/EIOPA_all_curves) since December 2014, in three CSV files

**Interest rates and economic scenarios**
- Vasicek (one- and two-factor), Hull-White one-factor and Dothan short-rate models
- Black-Scholes, correlated Brownian motion and binomial option pricing
- [A lightweight economic scenario generator](https://github.com/open-source-modelling/Light_Economic_Generator)
- [A validation framework for a monthly scenario generator](https://github.com/open-source-modelling/Validation_Economic_Stochastic_Generator), a reduced version of a framework built for an Italian bancassurance group

**Statistics and time series**
- Stationary bootstrap, with automatic block-length calibration
- Singular spectrum analysis

**Open data**
- [SFCR tables for 22 Italian life insurers](https://github.com/open-source-modelling/SFCR_using_Mistral_2025) (S.02.01, S.23.01, S.25.01), extracted with integrity checks
- Pipelines for [EDGAR sovereign emissions](https://github.com/open-source-modelling/EDGAR_pipeline) and [IMF PPP GDP](https://github.com/open-source-modelling/IMF_GDP_pipeline), for carbon-intensity reporting

Italian-language versions of several algorithms are in [assicurazione_python](https://github.com/open-source-modelling/assicurazione_python).

---

### AI workflows for actuarial teams

Teams are starting to use AI assistants such as Claude, Copilot and ChatGPT in their daily work, but there's been no shared place for insurance-specific tools. [insurance_skills](https://github.com/open-source-modelling/insurance_skills) is that place: an open collection of reusable assistant skills.

Every skill follows one rule. **The checks and calculations run in tested Python; the assistant is only the interface.** You ask in plain English, and the answer comes from code you can read, so the model can't make up a number.

| Skill | What it does |
|---|---|
| [historic-eiopa-yield-curve](https://github.com/open-source-modelling/eiopa-yield-curve-skill) | Returns any historic EIOPA risk-free rate curve, for any country, maturity and date since December 2014, including forwards, discount factors and stressed curves |
| [spontaneous-testing-for-excel](https://github.com/open-source-modelling/spontaneous-testing-for-excel) | You list tests for a workbook in plain English on a `TEST` sheet. The skill runs each one and writes back what it checked and whether it passed, without touching anything else |
| [validate-ul-fund-data](https://github.com/open-source-modelling/validate-ul-fund-data) | Runs 22 checks on the shape, types and internal consistency of a periodic fund data extract. It returns a pass/fail report and a SHA-256 fingerprint of the file, so bad data is caught before a re-run |
| [ranking_life_script](https://github.com/open-source-modelling/ranking_life_script) | Gives several AI models the same customer scenario and records how each one ranks a list of life insurers, and why. It measures how AI assistants perceive your company next to its peers |

AI also does the heavy lifting in our open data. The [SFCR tables](https://github.com/open-source-modelling/SFCR_using_Mistral_2025) are extracted from PDF reports with Mistral OCR, then validated with accounting integrity checks. Those checks have already caught a likely transposition error in a published report.

Each team's data is different, so fork a skill and adapt its rules. **Does your team have a skill that works well? Share it.** Contributions are very welcome.

---

### Using it in production?

Open code is where a model starts. Making it hold up in reporting takes more work: validation, integration and training. [Qnity Consultants](https://qnityconsultants.com) does exactly that for life insurers, pension funds and ALM teams in the UK and Europe:
- independent validation of scenario generators and yield curves
- moving Excel and VBA processes to Python
- asset-liability and TVOG modelling
- building AI assistant workflows that are auditable and can be reviewed like any other model
- training actuarial teams to maintain the models themselves

We work in English, Italian, German and Slovenian.

### Contributing

Suggestions, bug reports and new algorithms are welcome.
- **Found a bug or a question?** Open an issue on the relevant repository.
- **Have an implementation or an AI skill your team uses?** Get in touch and we'll help publish it in `insurance_skills`.

### Support

We support the Open Source Modelling development by taking paid project work through Qnity Consultants. For any referals, email gregor@osmodelling.com.

📧 gregor@osmodelling.com · [LinkedIn](https://www.linkedin.com/company/open-source-modelling) · [qnityconsultants.com](https://qnityconsultants.com)
