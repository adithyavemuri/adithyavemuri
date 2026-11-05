# Computational Scientist

**Atmospheric Physics · Wind Energy · Scientific Modelling & Tools**

I'm Adi, a computational scientist at KNMI with a PhD and research experience
in atmospheric flows, turbulence and numerical modelling.

My work focuses on understanding atmospheric processes and their applications
to wind energy through numerical simulations, physical analysis and
computational methods.

I develop scientific tools and reproducible modelling workflows that connect
atmospheric simulations, wind-energy analysis and physical diagnostics.
Together, these projects form the building blocks of an integrated atmospheric
and wind-energy modelling platform.

**Current focus:** physics-ensemble experiments, turbine-aware wind-farm
simulations and integrated atmospheric modelling workflows.

## Start here

**[WRF_tools](https://github.com/adithyavemuri/WRF_tools)** is the public entry
point: analyse existing WRF output, explore the diagnostics and see the results
without compiling or running a new simulation.

- **See the result:** [real-data demonstration PDF](https://github.com/adithyavemuri/WRF_tools/blob/main/example_results/final-report/hindcast-report.pdf).
- **Try it on your data:** [beginner examples](https://github.com/adithyavemuri/WRF_tools/blob/main/examples/README.md).
- **Prepare a simulation:** [TOML-driven ERA5 cases](https://github.com/adithyavemuri/wrf-era5-case) and [rootless WRF/WPS builds](https://github.com/adithyavemuri/wrf-autocompiler).

## How the pieces fit together

![Atmospheric modelling workflow: ERA5 and geodata preparation, WRF simulation, physical diagnostics, scientific reports and suitable WRF-LES inflow for OpenFAST](assets/modelling-workflow.svg)

The public packages run independently. A **private workflow prototype** connects
build, preparation, execution and reporting.

## Public building blocks

| Project | Role in the platform |
| --- | --- |
| **[wrf-autocompiler](https://github.com/adithyavemuri/wrf-autocompiler)** | Build WRF-ARW/WPS without root access, with configurable compiler, dependency and build-mode choices. |
| **[wrf-era5-case](https://github.com/adithyavemuri/wrf-era5-case)** | Download ERA5/geodata and generate readable WRF/WPS configuration from TOML, including stationary one-way nests. |
| **[WRF_tools](https://github.com/adithyavemuri/WRF_tools)** | Analyse WRF/WRF-LES output: meteorology, turbulence, wind energy, comparisons, visualisation, reports and TurbSim/OpenFAST inflow. |
| **[wrf-source-tools](https://github.com/adithyavemuri/wrf-source-tools)** | Inspect WRF Fortran interfaces, direct-call chains and selected assignments offline; support source-level investigation. |
| **[LocalHarness](https://github.com/adithyavemuri/LocalHarness)** | Set up local Qwen, Gemma and Phi models, with OpenCode, Cline support, shared skills and browser switching. Optional development support, not part of the numerical model. |

Each repository provides its own setup, editable examples and limitations.

## Short demonstration: WRF output → a scientific report

[![WRF_tools wind and boundary-layer diagnostics: map, vertical section, time-height evolution and profiles](https://raw.githubusercontent.com/adithyavemuri/WRF_tools/main/docs/demo/d02-wind-overview.png)](https://github.com/adithyavemuri/WRF_tools)

This **WRF_tools** figure combines a wind map, vertical section, time-height
evolution and profiles. The linked demonstration report uses a two-domain
Netherlands hindcast: 9 km and 3 km grids, 10 January 2025, 00–06 UTC.

To generate a report from your own output, clone `WRF_tools`, follow its
[installation guide](https://github.com/adithyavemuri/WRF_tools#installation),
then run from that repository:

```bash
python examples/create_hindcast_report.py /path/to/wrf/run \
  --domain d02 --diagnostics all --output reports/my-case
```

Open `reports/my-case/hindcast-report.pdf`. The report includes the domains
found in the run; `d02` selects the primary domain for this example. The same
workflow can be reused on another case rather than rewriting the analysis.

**Scientific scope:** these are model-based research workflows. Diagnostic
assumptions, sampling requirements and validation boundaries are documented in
the [methods and references](https://github.com/adithyavemuri/WRF_tools/blob/main/docs/SCIENTIFIC_METHODS.md).

## Supporting software: LocalHarness

[![Local model browser, an optional LocalHarness interface](assets/local-model-browser.png)](https://github.com/adithyavemuri/LocalHarness)

**[LocalHarness](https://github.com/adithyavemuri/LocalHarness)**, previously named
`qwen-local`, is a separate local AI project for software development. It handles
verified model downloads and local runtime/client setup.
OpenCode is the default coding client; Cline and the optional
[llama.cpp](https://github.com/ggml-org/llama.cpp) browser shown above are also
supported. See [platform support](https://github.com/adithyavemuri/LocalHarness/blob/main/SUPPORT.md)
for the tested compatibility boundary.

## Research interests

- Atmospheric boundary-layer dynamics and turbulence.
- Wind-farm wakes and atmosphere–turbine interactions.
- Numerical modelling, physics ensembles and model uncertainty.
- Physical interpretation and reproducible computational research.

## Connect

[LinkedIn](https://www.linkedin.com/in/adithyavemuri/) ·
[Explore my public repositories](https://github.com/adithyavemuri?tab=repositories)
