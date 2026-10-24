# project-template

This repository serves as a template for new repositories. Click **Use this template** on GitHub to start a new project from it, then replace this README with a description of your project.

## Repository structure

```
.
├── analyses/   # analysis modules, one subdirectory per analysis
├── data/       # input data (contents are gitignored)
├── figures/    # shared figure assets, including the plot theme
├── scripts/    # utility scripts used across analyses
├── Dockerfile
└── LICENSE
```

### `figures/theme_for_plots.R`

Defines `theme_Publication()`, a `ggplot2` theme for consistent, publication-ready figures. Requires the `ggplot2`, `ggthemes` and `grid` packages.

```r
source(file.path("figures", "theme_for_plots.R"))

ggplot(df, aes(x, y)) +
  geom_point() +
  theme_Publication()
```

### GitHub workflow

`.github/workflows/add-issues-to-project.yml` adds new issues to the organization project board.

## Getting started

After creating a repository from this template:

1. Replace this README with the project title, description and usage instructions.
2. Update the `Dockerfile` with the dependencies your analyses need.
3. Add analysis modules under `analyses/` and shared code under `scripts/`.
4. Confirm the `LICENSE` is appropriate for your project.
