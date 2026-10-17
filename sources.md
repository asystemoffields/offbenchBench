# Sources

Starting points for phase 1, not a closed list. Names and links change, so check that each one still exists before relying on it. If you find a good source that isn't here, suggest adding it. That is an easy first contribution to offbenchBench itself.

If the operator dispatched a problem, you don't need this file yet. Come back to it when checking what is known (phase 4, section 2).

## Open problems in mathematics

- **erdosproblems.com**, Thomas Bloom's catalogue of problems posed by Paul Erdős, each with a status, references and a forum thread. Read the forum's AI-contribution rules and the threads titled "AI Contributions" before doing anything. Its "open" means the maintainer wasn't aware of a solution.
- **Formal Conjectures** (github.com/google-deepmind/formal-conjectures): Lean 4 statements of open and solved conjectures, including many Erdős problems and OEIS conjectures, with source links. A formal statement is the best starting point for an attack, and a misformalization you find is itself a contribution.
- **The OEIS** (oeis.org): thousands of entries carry conjectures in their comments and formulas. Search for "conjecture" within an entry area you know. The OEIS has its own editorial process.
- **Open Problem Garden** (garden.irmacs.sfu.ca), **the Kourovka Notebook** (group theory), **Guy's *Unsolved Problems in Number Theory***, **the Scottish Book**, and the open-questions sections of surveys and recent papers in any area.
- **Wikipedia's lists of unsolved problems** by field, as an index into the literature, never as a source of status.
- **Terence Tao's blog** and the Polymath wiki, for problems with public, collaborative attack histories and clear accounts of what has been tried.

Watch for: problems that are obscure rather than hard, problems whose stated status is years old, problems with a finite computational component, and problems sitting next to one that recently fell.

## Open problems and open questions in science

- **Papers and surveys** that end with "open questions" or "future work", where the authors are reachable.
- **Replication and reproducibility efforts**: a published result that nobody has reproduced, with open data and code, is an open problem with a clear first move.
- **Benchmark and reference datasets with unexplained residuals**, anomalies flagged in survey papers, or discrepancies between two instruments or models.
- **Computational chemistry, materials, astronomy and genomics** all keep community lists of unsolved or contested cases; search the field's name with "open problems" or "unsolved".

## Crowdsourced and citizen science

Projects where volunteers do work by hand that tooling could make better, faster or more reliable, and whose science teams accept help.

- **Zooniverse** (zooniverse.org): hundreds of live projects, each with a science team, a talk board and a data policy. Tooling for the team, aggregation and quality analysis, or a reanalysis of published classification data are all plausible contributions. Model-generated classifications are not.
- **BOINC** projects and **Folding@home**: distributed computing with open client code and forums.
- **Breakthrough Listen** open data archive, and other public SETI and radio-transient datasets, for signal-processing and search-pipeline work.
- **eBird, iNaturalist, GBIF**: biodiversity data with open APIs and active research communities.
- **Galaxy Zoo, Planet Hunters, Radio Galaxy Zoo** and their published catalogues, for reanalysis.
- **OpenStreetMap, Wikidata, Wikimedia Commons** and the archives and museums that publish open collections: a lot of real work hides in their issue trackers and project pages.

## Empirical puzzles with open data

Lost ships and aircraft, unidentified signals, unattributed documents and artworks, unexplained observations. The first move is always the same: find who is actually working on it (a survey team, an archive, a museum, a project's science team), what has already been tried and recorded, and what open data exists (bathymetry, satellite imagery, digitised archives, catalogues). Good sources are the institution's own publications and open-data portals, national archive catalogues, GEBCO and NOAA bathymetry, Copernicus and Landsat imagery, and the published reports of previous searches. Treat anything from enthusiast forums as a lead to verify, not a fact.

## Scientific software and data

### Search patterns

GitHub CLI (`gh`). Adjust the owner, labels and topics:

```bash
# Unassigned help-wanted issues in one org, most recently active first
gh search issues --owner openclimatefix --state open --no-assignee \
  --label "help wanted" --sort updated --limit 30

# The same, without the label requirement
gh search issues --owner pvlib --state open --no-assignee --sort updated --limit 30

# Find active scientific repos by topic
gh search repos --topic climate-science --sort updated --limit 30
gh search repos --topic bioinformatics --sort updated --limit 30
```

Useful topics include `climate`, `weather`, `meteorology`, `hydrology`, `oceanography`, `remote-sensing`, `earth-observation`, `energy-systems`, `solar-energy`, `astronomy`, `astrophysics`, `bioinformatics`, `genomics`, `epidemiology`, `neuroscience`, `chemistry`, `molecular-dynamics`, `materials-science`, `ecology` and `citizen-science`.

On the web, phrases like "help wanted", "contributions welcome", "call for contributors", "we need help with" or "volunteers needed", combined with a field name, find calls outside GitHub: mailing lists, Discourse forums, project websites.

### Umbrella programs

- **NumFOCUS** sponsored and affiliated projects: numfocus.org/sponsored-projects
- **pyOpenSci** (pyopensci.org) and **rOpenSci** (ropensci.org), peer-reviewed scientific packages
- **OpenAstronomy** (openastronomy.org), which publishes contributor idea lists
- **Chan Zuckerberg Initiative**, Essential Open Source Software for Science grantees: chanzuckerberg.com/eoss
- **Google Summer of Code** organization and idea lists. Treat the ideas as problems maintainers want solved, whether or not GSoC is involved.
- **Software Sustainability Institute** (UK) and **US-RSE**, for research software communities

### By field (example GitHub orgs)

**Climate, weather and Earth observation:** `openclimatefix`, `pvlib`, `Unidata` (MetPy), `SciTools` (Iris, Cartopy; Met Office), `ecmwf`, `pangeo-data`, `pydata` (xarray), `NCAR`, `NOAA-EMC`, `NOAA-OWP`, `CliMA`, `E3SM-Project`, `ESMValGroup`, `DOI-USGS`, `nasa`

**Energy systems:** `PyPSA`, `NREL`, `open-energy-modelling` related projects, `openclimatefix`

**Astronomy and physics:** `astropy`, `sunpy`, `gwpy`, `scikit-hep`, `root-project`

**Life sciences and health:** `biopython`, `scverse`, `Bioconductor`, `galaxyproject`, `nextstrain`, `epiforecasts`, `AllenInstitute`

**Chemistry and materials:** `openmm`, `MDAnalysis`, `materialsproject`, `rdkit`

**Measurement and standards:** `usnistgov`

**Citizen science tooling:** `zooniverse`

### Government and national efforts

Many agencies publish code and take outside contributions, often more slowly than community projects. Look at code.gov-style catalogs, agency GitHub orgs (NASA, NOAA, USGS, NIST, the Met Office, ECMWF, ESA, and national weather and mapping services), and data-portal tooling. Expect stricter rules, such as a CLA or no PRs from forks. Check them during phase 1.

## Routine work

There is no source list for this. The operator brings it: their own project, a friend's game, a club's website. The protocol still applies, scaled down: measure before you change anything, verify after, and don't claim more than you measured.
