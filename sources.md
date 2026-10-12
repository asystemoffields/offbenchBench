# Sources

These are starting points for phase 1, not a closed list. Org names and links change, so check that each one still exists before relying on it. If you find a good source that isn't here, suggest adding it. That is an easy first contribution to offbenchBench itself.

## Search patterns

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

Useful topics to search include `climate`, `weather`, `meteorology`, `hydrology`, `oceanography`, `remote-sensing`, `earth-observation`, `energy-systems`, `solar-energy`, `astronomy`, `astrophysics`, `bioinformatics`, `genomics`, `epidemiology`, `neuroscience`, `chemistry`, `molecular-dynamics`, `materials-science`, `ecology` and `citizen-science`.

On the web, phrases like "help wanted", "contributions welcome", "call for contributors", "we need help with" or "volunteers needed", combined with a field name, find calls outside GitHub, such as mailing lists, Discourse forums and project websites.

## Umbrella programs (curated lists of real science projects)

- **NumFOCUS** sponsored and affiliated projects: numfocus.org/sponsored-projects
- **pyOpenSci**, peer-reviewed scientific Python packages: pyopensci.org
- **rOpenSci**, peer-reviewed scientific R packages: ropensci.org
- **OpenAstronomy**, which publishes contributor idea lists: openastronomy.org
- **Chan Zuckerberg Initiative**, Essential Open Source Software for Science grantees: chanzuckerberg.com/eoss
- **Google Summer of Code** organization and idea lists. Treat the ideas as a list of problems maintainers want solved, whether or not GSoC is involved.
- **Software Sustainability Institute** (UK) and **US-RSE**, for research software communities.

## By field (example GitHub orgs)

**Climate, weather and Earth observation:** `openclimatefix`, `pvlib`, `Unidata` (MetPy), `SciTools` (Iris, Cartopy; Met Office), `ecmwf`, `pangeo-data`, `pydata` (xarray), `NCAR`, `NOAA-EMC`, `NOAA-OWP`, `CliMA`, `E3SM-Project`, `ESMValGroup`, `DOI-USGS`, `nasa`

**Energy systems:** `PyPSA`, `NREL`, `open-energy-modelling` related projects, `openclimatefix`

**Astronomy and physics:** `astropy`, `sunpy`, `gwpy`, `scikit-hep`, `root-project`

**Life sciences and health:** `biopython`, `scverse`, `Bioconductor`, `galaxyproject`, `nextstrain`, `epiforecasts`, `AllenInstitute`

**Chemistry and materials:** `openmm`, `MDAnalysis`, `materialsproject`, `rdkit`

**Measurement and standards:** `usnistgov`

**Citizen science:** `zooniverse`

## Government and national efforts

Many agencies publish code and take outside contributions, though often more slowly than community projects. Look at code.gov-style catalogs, agency GitHub orgs (NASA, NOAA, USGS, NIST, the Met Office, ECMWF, ESA, and national weather and mapping services), and data-portal tooling. Expect stricter contribution rules, such as a CLA or no PRs from forks. Check them during phase 1.
