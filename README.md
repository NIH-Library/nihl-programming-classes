# NIH Library — Programming Trainings

This repository hosts materials for NIH Library programming trainings. It’s designed for reproducibility, so everyone can run the same code and get the same results.

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

These example use the URL for the [nihl-programming-classes](https://github.com/NIH-Library/nihl-programming-classes) repo.

### Option A — Git (command line)

``` bash
git clone https://github.com/NIH-Library/nihl-programming-classes.git
cd nihl-programming-classes
```

### Option B — RStudio

1.  Open RStudio → File ▸ New Project.
2.  Choose Version Control → Git.
3.  Repository URL: <https://github.com/NIH-Library/nihl-programming-classes.git>
4.  Project directory name: `nihl-prog-classes`
5.  Choose a parent directory (e.g., *Documents*).
6.  Click Create Project. RStudio will clone the repo and open it.

*Tip:* Ensure Git is installed and visible to RStudio (Tools ▸ Global Options ▸ Git/SVN).

### Option C — Downloading Project Structure Repo (recommended for class)

We have created a standalone folder structure that can be used for all of our programming classes:

1.  Download the following zipped folder to your computer.
2.  Unzip the folder in your documents folder.
3.  Deleted the zipped folder that you downloaded from GitHub.
4.  Instructions for opening and working with this project will be covered in the training.

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

## Repository Structure

The repository is organized into training-specific folders under `trainings/`. Each training folder follows a similar layout:

```         
trainings/
  nihl-ggplot-custom/
    handouts/     # slides and handouts
    images/       # images used in lessons
    docs/         # training-specific documentation not part of the training
    figures/      # generated figures/plots
    data-raw/     # original input data (read-only)
    data-output/  # processed/derived outputs
    src/          # training-specific source code or utilities
```

> Note: These are the recommended folder structures for our programming classes. You are free to use a different folder structure, but please keep this in mind during the live-coding sections of our trainings.
