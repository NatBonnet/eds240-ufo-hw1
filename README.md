# EDS 240: Data Visualization & Communication | Homework #1 (Interpreting `{ggplot2}` code)

## Author: Nathalie Bonnet

Instructor: Sam Shanny-Csik

Teaching Assistant: Annie Adams

## Description

This repository contains Nathalie Bonnet's work on [homework assignment #1](https://eds-240-data-viz.github.io/course-materials/assignments/HW1.html) for EDS 240 in Winter Quarter 2026.`HW1.qmd` was a pre-filled template file containing code originally created from Dan Oehm’s 2023 UFO Sightings visualization for [tidytuesday](https://github.com/rfordatascience/tidytuesday/blob/main/data/2023/2023-06-20/readme.md#data-dictionary), and adapted by Sam Shanny-Csik for teaching purposes. The goal of this exercise was to interpret and explain code written by another person.



## Folders and Files
- HW1files/libs: setup information for R
- fonts: contains font files for imported local font choices
- images: contains ufo image used in visualization
- outputs: destination for rendering final ggplot visualization

.gitignore: instructions for how the IDE should not track certain files like .DS_Store

HW1.qmd: template quarto document containing all previously written code, questions, and written responses, as well as any comments made during interpretation.

HW1.html: HTML file version of the quarto document information

README.md: repository documentation

## Data Access
These data are publicly accessible from the National UFO Reporting Center, and were further processed with data from sunrise-sunset.org by Jon Harmon [jonthe geek on GitHub](https://github.com/jonthegeek/apis/)

The author of the code provides this to access the data on the project's README:

```{r}
# Get the Data

# Read in with tidytuesdayR package 
# Install from CRAN via: install.packages("tidytuesdayR")
# This loads the readme and all the datasets for the week of interest

# Either ISO-8601 date or year/week works!

tuesdata <- tidytuesdayR::tt_load('2023-06-20')
tuesdata <- tidytuesdayR::tt_load(2023, week = 25)

ufo_sightings <- tuesdata$`ufo_sightings`
places <- tuesdata$`places`
day_parts_map <- tuesdata$`day_parts_map`

# Or read in the data manually

ufo_sightings <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2023/2023-06-20/ufo_sightings.csv')
places <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2023/2023-06-20/places.csv')
day_parts_map <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2023/2023-06-20/day_parts_map.csv')
```
## References
Dan Oehm’s 2023 UFO Sightings visualization for tidytuesday
  @misc{tidytuesday, 
    title = {Tidy Tuesday: A weekly social data project}, 
    author = {Data Science Learning Community}, 
    url = {https://tidytues.day}, 
    year = {2024} 
  }
[README](https://github.com/rfordatascience/tidytuesday/blob/e0def665954dab2fbd9fb92c15533b81009d3389/data/2023/2023-06-20/readme.md#data-dictionary)


