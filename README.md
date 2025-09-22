# NIH Library — Programming Trainings

This repository hosts materials for NIH Library programming trainings. It’s designed for reproducibility, so everyone can run the same code and get the same results.

Repo: <https://github.com/NIH-Library/nihlibrary-programming-classes.git>

------------------------------------------------------------------------

## Trainings in This Repo

-   [Taming Messy Data: Practical R Wrangling with the Tidyverse](https://www.nihlibrary.nih.gov/training/taming-messy-data-practical-r-wrangling-tidyverse-0)
-   [Data Visualization in R: Introduction to ggplot (Part 1 of 2)](https://www.nihlibrary.nih.gov/training/data-visualization-r-introduction-ggplot-part-1-2-2)
-   [Data Visualization in R: Customizations (Part 2 of 2)](https://www.nihlibrary.nih.gov/training/data-visualization-r-customizations-part-2-2-2)
-   [Introduction to Quarto for Scientific Writing](https://www.nihlibrary.nih.gov/training/introduction-quarto-scientific-writing)

Each training has its own folder under `trainings/`.

# Quick Start

## Install prerequisites

-   R (≥ 4.3) and Quarto (≥ 1.4)
-   RStudio (required; primary teaching environment)
-   Git
-   Python (≥ 3.11)
-   Optional: Conda (Miniconda/Anaconda)

## Clone the repository

### Option A — Git (command line)

``` bash
git clone https://github.com/NIH-Library/nihl-programming-classes.git
cd nihl-programming-classes
```

### Option B — RStudio (recommended for class)

1.  Open RStudio → File ▸ New Project…
2.  Choose Version Control → Git.
3.  Repository URL: `https://github.com/NIH-Library/nihl-programming-classes.git`
4.  Project directory name: `nihl-prog-classes`
5.  Choose a parent directory (e.g., *Documents*).
6.  Click Create Project. RStudio will clone the repo and open it.

*Tip:* Ensure Git is installed and visible to RStudio (Tools ▸ Global Options ▸ Git/SVN).

### Set up environments R setup (RStudio)

``` r
# In RStudio Console, install core packages used in trainings
pkgs <- c("tidyverse","ggplot2","readr","dplyr","quarto")
new <- setdiff(pkgs, rownames(installed.packages()))
if (length(new)) install.packages(new, repos = "https://cloud.r-project.org")
```

### Set up environments (to use R in Jupyter):

``` r
install.packages("IRkernel")
IRkernel::installspec()  # adds the R kernel to Jupyter
```

### Set up environments Python setup

OR venv + pip:

``` bash
python -m venv .venv
# macOS/Linux:
source .venv/bin/activate
# Windows:
.venv\Scripts\activate
pip install -r requirements.txt
```

### Open materials

`-   /trainings/nihl-wrangling-r/handouts`
`-   /trainings/nihl-ggplot-custom/handouts`
`-   /trainings/nihl-ggplot-intro/handouts`
`-   /trainings/nihl-quarto/handouts`