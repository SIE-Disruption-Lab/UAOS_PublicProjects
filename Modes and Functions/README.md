# Modes and Functions

Artifacts accompanying the paper:

> (prelim) Gregory, J. (2026). An Ontological Pattern for Spacecraft Operational Mode Management and Structural Validation. *Journal of Spacecraft and Rockets*. 

## Contents

| Folder | Description |
|--------|-------------|
| `CATSAT/` | CATSAT OML description model (`src/oml/`) and four SPARQL validation queries (`src/sparql/`) |
| `Biomass/` | Partial OML description model of the ESA Biomass mission (`src/oml/`) |
| `Dashboard/` | Standalone HTML validation dashboard |

The UAOS_Modes ontology (`UAOS_Modes.oml`) is included as a build dependency in both `CATSAT/build/oml/` and `Biomass/build/oml/`.

## Using the Dashboard

Open `Dashboard/dashboard.html` directly in a browser. Use the four file upload slots to load the JSON result files from `CATSAT/build/results/`. No web server is required.

## Queries

The four SPARQL queries are located in `CATSAT/src/sparql/`:

- `01_available_functions.sparql` — Q1: Available functions per mode (TransitionAvailability inference)
- `02_missing_sub_transitions.sparql` — Q2: Cross-level sub-transition semantic alignment
- `03_incomplete_transitions.sparql` — Q3: Transitions missing source or target mode declarations
- `04_chain_step_never_available.sparql` — Q4: Functional chain steps with no valid execution mode
