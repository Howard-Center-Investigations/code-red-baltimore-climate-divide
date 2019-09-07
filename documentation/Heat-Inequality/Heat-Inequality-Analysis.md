-   [Introduction](#introduction)
-   [Links to Data, Cleaning and Analysis Scripts, RMarkdown HTML Pages](#links-to-data-cleaning-and-analysis-scripts-rmarkdown-html-pages)
    -   [Load packages](#load-packages)
    -   [Load variables and data](#load-variables-and-data)
-   [Line-By-Line Fact-Check](#line-by-line-fact-check)
    -   [Fact: 11-Day Heat Wave \[cq\]](#fact-11-day-heat-wave-cq)
    -   [Fact: Temperature inside and outside Tammy Jackson's home \[cq\]](#fact-temperature-inside-and-outside-tammy-jacksons-home-cq)
    -   [Fact: Outdoor temperature in Baltimore on August 1, 2019 at 11:20 a.m. \[cq\]](#fact-outdoor-temperature-in-baltimore-on-august-1-2019-at-1120-a.m.-cq)
    -   [Fact: Average annual temperature increase in U.S., Baltimore \[cq\]](#fact-average-annual-temperature-increase-in-u.s.-baltimore-cq)
    -   [Fact: Projected increase in hot days in Baltimore \[cq\]](#fact-projected-increase-in-hot-days-in-baltimore-cq)
    -   [Fact: Heat index on first floor of Tammy Jackson's home \[cq\]](#fact-heat-index-on-first-floor-of-tammy-jacksons-home-cq)
    -   [Fact: 8 Degree F difference between hottest and coolest neighborhoods \[cq\]](#fact-8-degree-f-difference-between-hottest-and-coolest-neighborhoods-cq)
    -   [Fact: Heat and poverty, life expectancy, crime, unemployment \[cq\]](#fact-heat-and-poverty-life-expectancy-crime-unemployment-cq)
    -   [Fact: McElderry Park is the hottest neighborhood in Baltimore \[cq\]](#fact-mcelderry-park-is-the-hottest-neighborhood-in-baltimore-cq)
    -   [Fact: Heat and chronic illness \[cq\]](#fact-heat-and-chronic-illness-cq)
    -   [Fact: Frequency of EMS Calls Increase with Temperature \[cq\]](#fact-frequency-of-ems-calls-increase-with-temperature-cq)
    -   [Fact: Hot neighborhoods have lower incomes \[cq\]](#fact-hot-neighborhoods-have-lower-incomes-cq)
    -   [Fact: More affluent communities have more trees \[cq\]](#fact-more-affluent-communities-have-more-trees-cq)
    -   [Fact: Crime rates higher in poorer neighborhoods \[cq\]](#fact-crime-rates-higher-in-poorer-neighborhoods-cq)
    -   [Fact: Highest temperature, humidity sensor values \[cq\]](#fact-highest-temperature-humidity-sensor-values-cq)
    -   [Fact: Hotter inside than outside \[cq\]](#fact-hotter-inside-than-outside-cq)
    -   [Fact: Tammy Jackson's house on July 21 \[cq\]](#fact-tammy-jacksons-house-on-july-21-cq)
    -   [Fact: Hotter inside Stephanie Pingley's house than outside \[cq\]](#fact-hotter-inside-stephanie-pingleys-house-than-outside-cq)
    -   [Fact: Hottest seven-day stretch of the summer \[cq\]](#fact-hottest-seven-day-stretch-of-the-summer-cq)
    -   [Fact: Heat index on July 21 \[cq\]](#fact-heat-index-on-july-21-cq)
    -   [Fact: Heat index in the bedroom \[cq\]](#fact-heat-index-in-the-bedroom-cq)
    -   [Fact: Minimum heat index in Pingley bedroom \[cq\]](#fact-minimum-heat-index-in-pingley-bedroom-cq)
    -   [Fact: Heat index indoors and out \[cq\]](#fact-heat-index-indoors-and-out-cq)
    -   [Fact: Outdoor heat index on July 19](#fact-outdoor-heat-index-on-july-19)
    -   [Fact: Indoor heat index on July 19 \[cq\]](#fact-indoor-heat-index-on-july-19-cq)
    -   [Fact: Heat index Baltimore July 20 \[cq\]](#fact-heat-index-baltimore-july-20-cq)
    -   [Fact: Heat index in Pingley's house July 20 \[cq\]](#fact-heat-index-in-pingleys-house-july-20-cq)
    -   [Fact: Heat index Michael Thomas and Alberta Wilkerson \[cq\]](#fact-heat-index-michael-thomas-and-alberta-wilkerson-cq)
    -   [Fact: tree canopy on McElderry Park neighborhood \[cq\]](#fact-tree-canopy-on-mcelderry-park-neighborhood-cq)
    -   [Fact: East Baltimore Tree Cover \[cq\]](#fact-east-baltimore-tree-cover-cq)

Introduction
------------

This R markdown document describes a portion of the data analysis for a reporting project examining the effects of climate-change driven temperature increases on the health of people who live in cities. The project was done in partnership with the [University of Maryland Philip Merrill College of Journalism](https://merrill.umd.edu/), [Capital News Service](https://cnsmaryland.org/), [the Howard Center for Investigative Journalism](https://merrill.umd.edu/about-merrill/signature-programs/the-howard-center-for-investigative-journalism/), [NPR](https://www.npr.org/), [Wide Angle Youth Media](https://www.wideanglemedia.org/) and [WMAR](https://www.wmar2news.com/). It also moved on the Associated Press wire.

For each sentence in the story "[Heat & Inequality: In Baltimore, the burden of rising temperatures isn’t shared](https://cnsmaryland.org/interactives/summer-2019/code-red/neighborhood-heat-inequality.html)" based on Howard Center data analysis, this document provides the original fact, the code and code output that support that fact, and an explanation where necessary.

Here are links to stories in the series published by participating organizations:

**CNSMaryland**

-   [Code Red: Baltimore's Climate Divide](https://cnsmaryland.org/interactives/summer-2019/code-red/introduction.html)
-   [Heat & Inequality: In Baltimore, the burden of rising temperatures isn’t shared](https://cnsmaryland.org/interactives/summer-2019/code-red/neighborhood-heat-inequality.html)
-   [Heat & Health: For people with chronic health conditions, heat and humidity are more than a summer nuisance](https://cnsmaryland.org/interactives/summer-2019/code-red/heat-health.html)
-   [The Role of Trees: No trees, no shade, no relief as climate heats up](https://cnsmaryland.org/interactives/summer-2019/code-red/role-of-trees.html)
-   [Seeking Solutions: Are government leaders and residents ready to act?](https://cnsmaryland.org/interactives/summer-2019/code-red/city-climate-future.html)
-   [Behind The Scenes: A look at how and why we reported the series](https://cnsmaryland.org/interactives/summer-2019/code-red/behind-scenes.html)

**NPR**

-   [As Rising Heat Bakes U.S. Cities, The Poor Often Feel It Most](https://www.npr.org/2019/09/03/754044732/as-rising-heat-bakes-u-s-cities-the-poor-often-feel-it-most)
-   [Trees Are Key To Fighting Urban Heat — But Cities Keep Losing Them](https://www.npr.org/2019/09/04/755349748/trees-are-key-to-fighting-urban-heat-but-cities-keep-losing-them)
-   [How High Heat Can Impact Mental Health](https://www.npr.org/templates/story/story.php?storyId=757034136&live=1)

**WMAR**

-   [Baltimore neighborhood identified as 'ground zero' for local effects of climate crisis](https://www.wmar2news.com/news/region/baltimore-city/baltimore-neighborhood-identified-as-ground-zero-for-local-effects-of-climate-crisis)

**Associated Press**

-   [Investigation: Urban poor hit hardest as the planet heats up](https://www.apnews.com/52ffefa9ecf144d1b9aec367cc52ea74)
-   [As temperatures rise, overdoses and hospital visits increase](https://www.apnews.com/4d83616b5ecd46d5896d274a37b39de9)
-   [No trees, no shade, no relief in cities as climate heats up](https://www.apnews.com/bebe7895ce374f6f9070fe69ab557c4f)

Links to Data, Cleaning and Analysis Scripts, RMarkdown HTML Pages
------------------------------------------------------------------

-   The entire codebase for this analysis, including R markdown cleaning and analysis scripts -- and the raw and cleaned data needed to reproduce the cleaning and analysis, is available through the [Howard Center's GitHub](https://github.com/Howard-Center-Investigations/Code-Red-Baltimore-Climate-Divide).
-   [Repo Readme](https://github.com/Howard-Center-Investigations/Code-Red-Baltimore-Climate-Divide/README.md)
-   Data
    -   [Data cleaning script](https://github.com/Howard-Center-Investigations/Code-Red-Baltimore-Climate-Divide/documentation/Data-Cleaning/Data-Cleaning.Rmd)
    -   [Raw data folder](https://github.com/Howard-Center-Investigations/Code-Red-Baltimore-Climate-Divide/data/input-data)
    -   [Cleaned data folder](https://github.com/Howard-Center-Investigations/Code-Red-Baltimore-Climate-Divide/data/putput-data)
-   Analysis
    -   [Analysis for NPR](https://github.com/Howard-Center-Investigations/Code-Red-Baltimore-Climate-Divide/documentation/NPR/NPR-Analysis.Rmd)
    -   [Heat and inequality story analysis](https://github.com/Howard-Center-Investigations/Code-Red-Baltimore-Climate-Divide/documentation/Heat-Inequality/Heat-Inequality-Analysis.Rmd)
    -   [Heat and health story analysis](https://github.com/Howard-Center-Investigations/Code-Red-Baltimore-Climate-Divide/documentation/Heat-Health/Heat-Health-Analysis.Rmd)
    -   [Role of trees story analysis](https://github.com/Howard-Center-Investigations/Code-Red-Baltimore-Climate-Divide/documentation/Role-of-Trees/Role-of-Trees-Analysis.Rmd)
-   A site with HTML versions of the R markdown files, for fact-checking the completed the analysis.
-   [Landing page](https://howard-center-investigations.github.io/code-red-baltimore-climate-divide/index.html)
-   [Data cleaning script](https://howard-center-investigations.github.io/code-red-baltimore-climate-divide/Data-Cleaning.html)
-   [Analysis for NPR](https://howard-center-investigations.github.io/code-red-baltimore-climate-divide/NPR-Analysis.html)
-   [Heat and inequality story analysis](https://howard-center-investigations.github.io/code-red-baltimore-climate-divide/Heat-Inequality-Analysis.html)
-   [Heat and health story analysis](https://howard-center-investigations.github.io/code-red-baltimore-climate-divide/Heat-Health-Analysis.html)
-   [Role of trees story analysis](https://howard-center-investigations.github.io/code-red-baltimore-climate-divide/Role-of-Trees-Analysis.html)
-   NPR has made available a separate GitHub repo for nationwide analysis on urban heat islands available [here](https://github.com/nprapps/heat-income).

### Load packages

``` r
#######################
#### Load Packages ####
#######################
# For debugging rm(list=ls())

library(tidyverse) # For general data science goodness
library(corrr) # For correlation goodness
library(lubridate) # For working with that datetime
library(broom) # For converting lm output to dataframe
library(TTR) # For moving averages

# Turn off scientific notation in RStudio (prevents coersion to character type)
options(scipen = 999)
```

### Load variables and data

``` r
#########################
#### Store Variables ####
#########################

# Common path to output data folder
path_to_data <- "../../data/output-data/"

###################
#### Load Data ####
###################

### Indoor temperature and humidity sensor data

# Michael and Alberta
folder <- "temperature_sensors/michael/"
michael_day_hourly_averages <- read_csv(paste0(path_to_data, folder, "michael_day_hourly_averages.csv"))
michael_day_minute_averages <- read_csv(paste0(path_to_data, folder, "michael_day_minute_averages.csv"))

# Stephanie and family
folder <- "temperature_sensors/stephanie/"
stephanie_day_minute_averages <- read_csv(paste0(path_to_data, folder, "stephanie_day_minute_averages.csv"))
stephanie_day_hourly_averages <- read_csv(paste0(path_to_data, folder, "stephanie_day_hourly_averages.csv"))

# Audrey
folder <- "temperature_sensors/audrey/"
audrey_day_minute_averages <- read_csv(paste0(path_to_data, folder, "audrey_day_minute_averages.csv"))
audrey_day_hourly_averages <- read_csv(paste0(path_to_data, folder, "audrey_day_hourly_averages.csv"))

# Tammy
folder <- "temperature_sensors/tammy/"
tammy_day_minute_averages <- read_csv(paste0(path_to_data, folder, "tammy_day_minute_averages.csv"))
tammy_day_hourly_averages <- read_csv(paste0(path_to_data, folder, "tammy_day_hourly_averages.csv"))

### Outdoor temperature data

# Inner Harbor temperature data
folder <- "baltimore_weather_stations/"
dmh <- read_csv(paste0(path_to_data, folder, "dmh.csv"))

# Historical temperature data, Baltimore and U.S.
folder <- "1895-2019-average-temperature/"
us_change_temp <- read_csv(paste0(path_to_data, folder, "us_change_temp.csv"))
baltimore_change_temp <- read_csv(paste0(path_to_data, folder, "baltimore_change_temp.csv"))

# Heat index projections
folder <- "heat_index_projections/"
heat_index_projections <- read_csv(paste0(path_to_data, folder, "heat_index_projections.csv"))

### Urban heat island, tree canopy, demographics data
folder <- "tree_temp_demographics/"

# Neighborhood geography
nsa_tree_temp <- read_csv(paste0(path_to_data, folder, "nsa_tree_temp.csv"))

# Community statistical area geography
csa_tree_temp_demographics <- read_csv(paste0(path_to_data, folder, "csa_tree_temp_demographics.csv"))

# Blocks geography
blocks_tree_temp_demographics <- read_csv(paste0(path_to_data, folder, "blocks_tree_temp_demographics.csv"))

### Hospital data
folder <- "hospital_data/"

# Inpatient admissions data
ip_full_zip_correlation_matrix <- read_csv(paste0(path_to_data, folder, "ip/ip_full_zip_correlation_matrix.csv"))

# Emergency room admissions data
op_er_full_zip_correlation_matrix <- read_csv(paste0(path_to_data, folder, "op_er/op_er_full_zip_correlation_matrix.csv"))

### EMS Data
folder <- "ems/"
dmh_ems <- read_csv(paste0(path_to_data, folder, "dmh_ems.csv"))
EMS_all <- read_csv(paste0(path_to_data, folder, "EMS_all.csv"))
```

Line-By-Line Fact-Check
-----------------------

### Fact: 11-Day Heat Wave \[cq\]

"So as a dangerous 11-day heat wave tormented the city in July, the hottest month ever recorded on the planet, fewer and fewer residents were going outside."

#### Explanation \[cq\]

Over an 11-day period in July 2019 -- July 12 through July 22 -- each day during that stretch had a maximum temperature of at least 90 degrees F and maximum heat index values of at least 92 degrees F. This was measured at a National Weather Service monitoring station located in the Inner Harbor.

#### Supporting code and output \[cq\]

``` r
 dmh %>%
  filter(month == 7,
         year == 2019,
         day >= 12,
         day <= 22) %>%
  group_by(`date`) %>%
  summarise(min_temp = min(avg_hourly_temperature_dmh),
            max_temp = max(avg_hourly_temperature_dmh),
            mean_temp = mean(avg_hourly_temperature_dmh),
            min_heat_index = min(avg_hourly_heat_index_dmh),
            max_heat_index = max(avg_hourly_heat_index_dmh),
            mean_heat_index = mean(avg_hourly_heat_index_dmh)
  ) %>%
  select(date, max_temp, max_heat_index)
```

    ## # A tibble: 11 x 3
    ##    date       max_temp max_heat_index
    ##    <date>        <dbl>          <dbl>
    ##  1 2019-07-12     90               92
    ##  2 2019-07-13     91               92
    ##  3 2019-07-14     93.9             98
    ##  4 2019-07-15     90               93
    ##  5 2019-07-16     96.1            104
    ##  6 2019-07-17     98.1            110
    ##  7 2019-07-18     93.9            103
    ##  8 2019-07-19     98.1            108
    ##  9 2019-07-20     99              108
    ## 10 2019-07-21    100              111
    ## 11 2019-07-22     96.1            104

### Fact: Temperature inside and outside Tammy Jackson's home \[cq\]

“Can’t even put your head out the door,” said Tammy Jackson, 48, on a day when the temperature outside hit 100 degrees Fahrenheit and 92 degrees in her home. “This is too much. Oh Lord, this is too much.”

#### Explanation \[cq\]

Tammy Jackson, a resident of Baltimore's McElderry Park neighborhood, had a temperature and humidity sensor installed in her house by our reporters. In her home, the highest temperature reading on Saturday, July 20, the day referenced in the story, was 92 degrees (91.6 degrees F).

For outdoor temperature, in most of our analysis, we used hourly snapshot readings taken at a National Weather Service monitoring station in the Inner Harbor. As the table below shows, the highest hourly reading in that data set on July 20 was 99 degrees. But the NWS official daily summary for that monitoring station -- which incorporates all readings taken, not just hourly snapshots -- indicates it did hit 100 degrees at some point on July 20. The data [can be viewed here](https://www.ncdc.noaa.gov/cdo-web/datasets/GHCND/stations/GHCND:USW00093784/detail).

#### Supporting code and output \[cq\]

``` r
# Max temperature in Jackson's House on July 20

tammy_day_hourly_averages %>%
  mutate(date = date(date_hour)) %>%
  filter(date == "2019-07-20") %>%
  group_by(date) %>%
  summarise(max_indoor_temperature = max(mean_indoor_temperature))
```

    ## # A tibble: 1 x 2
    ##   date       max_indoor_temperature
    ##   <date>                      <dbl>
    ## 1 2019-07-20                   91.6

``` r
# Max temperature outside on July 20
dmh %>%
 filter(month == 7,
         year == 2019,
        day == 20) %>%
  group_by(`date`) %>%
  summarise(max_temp = max(avg_hourly_temperature_dmh))
```

    ## # A tibble: 1 x 2
    ##   date       max_temp
    ##   <date>        <dbl>
    ## 1 2019-07-20       99

### Fact: Outdoor temperature in Baltimore on August 1, 2019 at 11:20 a.m. \[cq\]

"The graphic below shows temperatures in the 500 block of North Milton Street in McElderry Park at 11:20 a.m. on a summer morning in August."

#### Explanation \[cq\]

The date and time referenced in the graphic was 11:20 a.m. on August 1, 2019. To get the outdoor temperature we used the NWS hourly snapshots at the Inner Harbor monitoring station. In the 11 a.m. hour, it was 87.1 degrees.

#### Supporting code and output \[cq\]

``` r
dmh %>%
 filter(month == 8,
         year == 2019,
         day == 1,
         hour == 11) %>%
  select(date, avg_hourly_temperature_dmh)
```

    ## # A tibble: 1 x 2
    ##   date       avg_hourly_temperature_dmh
    ##   <date>                          <dbl>
    ## 1 2019-08-01                       87.1

### Fact: Average annual temperature increase in U.S., Baltimore \[cq\]

"Average annual temperatures in Baltimore have gone up more than 3 degrees over the last century, nearly twice as much as the rest of the country."

#### Explanation \[cq\]

To compute this average annual temperature change over the last century, we pulled historical average annual temperatures between 1895 and 2018, and the amount each annual average departed from the overall mean temperature during that period. The data for Baltimore and the U.S. came from the National Climactic Data Center. We used linear regression to examine the trend and produce a line of best fit through plotted points. We took the slope of the line of best fit and multiplied it by the number of years to arrive at the temperature increase over that period for Baltimore (3.4 degrees F), the U.S. (1.9 degrees F) and the difference between the two. Baltimore increased by 3.4 degrees F, 80 percent (nearly twice as much) as the U.S. (1.9 percent). A note: we got the idea to use this method from the excellent Washington Post interactive ["2°C: BEYOND THE LIMIT"](https://www.washingtonpost.com/graphics/2019/national/climate-environment/climate-change-america/), which arrived at the same figures as we did for Baltimore and the U.S.

#### Supporting code and output \[cq\]

``` r
# Create linear model showing trend of change in annual average temperature change 1895-2018 for the US
us_lm <- lm(anomaly ~ date, data = us_change_temp)

# Get the slope of the line of best fit from the linear model
us_slope <- tidy(us_lm) %>%
  filter(term == "date") %>%
  mutate(location = "us") %>%
  select(location, estimate) %>%
  rename(slope = estimate)

# Get the number of yearly observations from original data
us_years_count <- us_change_temp %>%
  # group_by(date) %>%
  summarise(years_count= n()) %>%
  mutate(location = "us") %>%
  select(location, years_count)

# Calculate degrees change
us_historical_change <- us_years_count %>%
  left_join(us_slope, by = "location") %>%
  mutate(change_degrees = years_count * slope)

# Create linear model showing trend of change in annual average temperature change 1895-2018 for Baltimore
baltimore_lm <- lm(anomaly ~ date, data = baltimore_change_temp)

# Get the slope of the line of best fit from the linear model
baltimore_slope <- tidy(baltimore_lm) %>%
  filter(term == "date") %>%
  mutate(location = "baltimore") %>%
  select(location, estimate) %>%
  rename(slope = estimate)

# Get the number of yearly observations from original data
baltimore_years_count <- baltimore_change_temp %>%
  # group_by(date) %>%
  summarise(years_count= n()) %>%
  mutate(location = "baltimore") %>%
  select(location, years_count)

# Calculate degrees change
baltimore_historical_change <- baltimore_years_count %>%
  left_join(baltimore_slope, by = "location") %>%
  mutate(change_degrees = years_count * slope)

# Bind together US and Baltimore
us_baltimore <- bind_rows(baltimore_historical_change, us_historical_change)

# Show change degrees and diference between two values as percentage
difference <- us_baltimore %>%
  select(location, change_degrees) %>%
  tidyr::spread(location, change_degrees) %>%
  mutate(difference = (baltimore-us)/us)

difference
```

    ## # A tibble: 1 x 3
    ##   baltimore    us difference
    ##       <dbl> <dbl>      <dbl>
    ## 1      3.41  1.89      0.804

### Fact: Projected increase in hot days in Baltimore \[cq\]

"And the planet’s warming has gained momentum, say researchers who estimate the number of very hot days in Baltimore could increase six-fold by the middle of the century."

#### Explanation \[cq\]

The Union of Concerned Scientists \[Killer Heat in the United States\] \[study\](<https://www.ucsusa.org/sites/default/files/attach/2019/07/killer-heat-analysis-full-report.pdf>) released this summer included detailed tables projecting the number of days of 100+ heat index days for most U.S. cities, and projected how many additional days of 100+ heat index days there would be by mid-century. They found there were six days of 100+ heat index days per year historically in Baltimore, and by mid-century there would be 37 days, a 6x increase. Note: our own analysis of historical Baltimore heat index data at a NWS Inner Harbor monitoring station found that the 6 days per year figure was likely a conservative estimate.

#### Supporting code and output \[cq\]

``` r
heat_index_projections %>%
  select(state, city, historical_100_plus, midcentury_no_action_100_plus) %>%
  filter(state == "MD", city == "Baltimore") %>%
  mutate(increase_x = midcentury_no_action_100_plus/historical_100_plus)
```

    ## # A tibble: 1 x 5
    ##   state city      historical_100_pl… midcentury_no_action_100_p… increase_x
    ##   <chr> <chr>                  <dbl>                       <dbl>      <dbl>
    ## 1 MD    Baltimore                  6                          37       6.17

### Fact: Heat index on first floor of Tammy Jackson's home \[cq\]

"Photo caption: The heat index on the first floor of Tammy Jackson’s McElderry Park home registered 93 degrees, 9 degrees hotter than it was outside, at 10 p.m. Sunday, July 21. Jackson has several grandchildren with asthma."

#### Explanation \[cq\]

Tammy Jackson, a resident of Baltimore's McElderry Park neighborhood, had a temperature and humidity sensor installed in her house by our reporters. In her home, at 10 p.m. on Sunday, July 21, the heat index was 93 degrees F, 9 degrees hotter than the outside heat index of 84 degrees.

#### Supporting code and output \[cq\]

``` r
tammy_day_hourly_averages %>%
  mutate(date = date(date_hour)) %>%
  mutate(hour = hour(date_hour)) %>%
  filter(date == "2019-07-21") %>%
  filter(hour == 22) %>%
  select(date, mean_indoor_heat_index, mean_outdoor_heat_index, indoor_heat_index_difference)
```

    ## # A tibble: 1 x 4
    ##   date       mean_indoor_heat_i… mean_outdoor_heat_i… indoor_heat_index_di…
    ##   <date>                   <dbl>                <dbl>                 <dbl>
    ## 1 2019-07-21                  93                   84                     9

### Fact: 8 Degree F difference between hottest and coolest neighborhoods \[cq\]

"Researchers at Portland State University in Oregon and the Science Museum of Virginia have mapped these areas, called urban heat islands, and data shows that temperatures here and in surrounding neighborhoods can run 8 degrees F hotter than in communities that have more trees and less pavement."

#### Explanation \[cq\]

The researchers took detailed measurements of Baltimore's urban heat island on August 29, 2018, and found differences across the city. Using the mean afternoon temperature for each neighborhood (excluding the representation of Leakin Park in our data -- we found the coolest neighborhood was Dickeyville (91 degrees F) and the hottest was McElderry Park (99.4 degrees F), a difference of 8.4 degrees F.

#### Supporting code and output \[cq\]

``` r
nsa_tree_temp %>%
  select(nsa_name, temp_mean_aft) %>%
  filter(nsa_name != "gwynns falls/leakin park") %>%
  filter((temp_mean_aft == min(temp_mean_aft)) | (temp_mean_aft == max(temp_mean_aft))) %>%
  arrange(desc(temp_mean_aft)) %>%
  tidyr::spread(nsa_name, temp_mean_aft) %>%
  mutate(difference_coolest_hottest = `mcelderry park`-`dickeyville`)
```

    ## # A tibble: 1 x 3
    ##   dickeyville `mcelderry park` difference_coolest_hottest
    ##         <dbl>            <dbl>                      <dbl>
    ## 1        91.0             99.4                       8.39

### Fact: Heat and poverty, life expectancy, crime, unemployment \[cq\]

"Graphic Caption: People who live in the hottest parts of the city are more likely to be poor, to live shorter lives, and to experience higher rates of violent crime and unemployment."

#### Explanation \[cq\]

In Baltimore's "community statistical areas", we examined the relationship between heat (mean afternoon temperature in our urban heat island data) and poverty, life expectancy, unemployment rates and violent crime by computing the correlation coefficient (r) for each metric. An r of 1 would indicate a perfect positive linear relationship and an r of -1 would indicate a perfect negative linear relationship and 0 indicating no relationship. There were moderate correlations with poverty (r =.4), violent crime (r=.58), life expectancy (r=-.41), and the unemployment rate (r=.32).

A table with the values used in the graphic is also displayed below. The same table is used in the scatterplot graphics that appear lower in the story.

#### Supporting code and output \[cq\]

``` r
# Correlation coefficients
csa_tree_temp_demographics %>%
  select_if(is.numeric) %>%
  as.matrix() %>%
  correlate() %>%
  focus(matches("temp_")) %>%
  mutate(variable=rowname) %>%
  select(variable, temp_mean_aft) %>%
  filter(str_detect(variable, "households_living|violent|life|unemployment"))
```

    ## # A tibble: 4 x 2
    ##   variable                                                   temp_mean_aft
    ##   <chr>                                                              <dbl>
    ## 1 percent_of_family_households_living_below_the_poverty_line         0.398
    ## 2 violent_crime_rate_per_1_000_residents                             0.580
    ## 3 life_expectancy                                                   -0.409
    ## 4 unemployment_rate                                                  0.316

``` r
# Graphic table
csa_tree_temp_demographics %>%
  select(csa2010, temp_mean_aft, matches("households_living|violent|life|unemployment"))
```

    ## # A tibble: 55 x 6
    ##    csa2010 temp_mean_aft percent_of_fami… violent_crime_r… life_expectancy
    ##    <chr>           <dbl>            <dbl>            <dbl>           <dbl>
    ##  1 allend…          94.0            20.7              19.4            69.6
    ##  2 beechf…          92.6            10.5              11.0            73.4
    ##  3 belair…          95.1            20.3              19.3            70.5
    ##  4 brookl…          95.0            24.2              29.9            69.2
    ##  5 canton           95.3             3.66             10.4            79.8
    ##  6 cedoni…          94.4            12.2              15.6            72.2
    ##  7 cherry…          95.0            39.3              26.7            70  
    ##  8 chinqu…          93.8            10.1              10.6            75.3
    ##  9 clarem…          94.6            24                15.8            70.5
    ## 10 clifto…          96.7            27.6              25.1            67.6
    ## # … with 45 more rows, and 1 more variable: unemployment_rate <dbl>

### Fact: McElderry Park is the hottest neighborhood in Baltimore \[cq\]

"McElderry Park, which despite its lyrical name offers little green space, is one of these: the hottest neighborhood in Baltimore, a city whose climate has long been classified as humid subtropical."

#### Explanation \[cq\]

Using the mean afternoon temperature in the urban heat island study, McElderry Park was the city's hottest neighborhood, with a mean afternoon temperature of 99.4 degrees F.

#### Supporting code and output \[cq\]

``` r
nsa_tree_temp %>%
  select(nsa_name, temp_mean_aft) %>%
  arrange(desc(temp_mean_aft))
```

    ## # A tibble: 278 x 2
    ##    nsa_name              temp_mean_aft
    ##    <chr>                         <dbl>
    ##  1 mcelderry park                 99.4
    ##  2 milton-montford                99.3
    ##  3 patterson place                98.6
    ##  4 dunbar-broadway                98.3
    ##  5 ellwood park/monument          98.3
    ##  6 penn-fallsway                  98.3
    ##  7 pleasant view gardens          98.3
    ##  8 madison-eastend                97.9
    ##  9 old goucher                    97.9
    ## 10 biddle street                  97.9
    ## # … with 268 more rows

### Fact: Heat and chronic illness \[cq\]

"Residents in the hottest areas have higher rates of chronic illnesses affected by heat, including asthma and COPD."

#### Explanation \[cq\]

We used condition prevalence rates from inpatient hospital admissions and emergency room visits, which are only available by ZIP code, and the median afternoon temperature of Baltimore ZIP codes, as calculated in the urban heat island data to examine relationships. The correlation coefficient for people diagnosed with asthma during hospital visits (r=.56) and emergency room visits (r=.49), and people diagnosed with COPD during hospital visits (r=.67) and emergency room visits (r=.57), indicated a moderate to strong positive relationship between heat and asthma and copd rates. This is not causal. In hotter areas, rates of asthma and copd are higher, and vice versa.

#### Supporting code and output \[cq\]

``` r
ip_full_zip_correlation_matrix %>%
    filter(str_detect(rowname, "asthma|copd")) %>%
    select(rowname, temp_median_aft)
```

    ## # A tibble: 2 x 2
    ##   rowname     temp_median_aft
    ##   <chr>                 <dbl>
    ## 1 copd_prev             0.673
    ## 2 asthma_prev           0.559

``` r
op_er_full_zip_correlation_matrix %>%
    filter(str_detect(rowname, "asthma|copd")) %>%
    select(rowname, temp_median_aft)
```

    ## # A tibble: 2 x 2
    ##   rowname     temp_median_aft
    ##   <chr>                 <dbl>
    ## 1 copd_prev             0.570
    ## 2 asthma_prev           0.489

### Fact: Frequency of EMS Calls Increase with Temperature \[cq\]

"In hot weather, emergency medical calls for some chronic conditions increase. The rate of emergency medical calls for cardiac arrest and congestive heart failure, for example, nearly double when the heat index hits 103 degrees."

#### Explanation \[cq\]

By merging a dataset of EMS calls with a dataset of hourly Baltimore heat index values, we were able to determine the heat index at the time of each EMS call during summer 2018. We looked at select conditions affected by heat, and compared how call rates changed when it was very hot -- over 103 heat index, a level defined by NWS as "dangerous -- and when the heat index was under 80. The second and third columns below reflect the number of hours that passed between calls (on average) when the heat index was below 80 degrees or above 103 degrees.

For example, when the heat index was above 103, there was a call for cardiac arrest every 2.94 hours. When the heat index was under 80, the calls happened less frequently, every 5.3 hours. That meant there were 80 percent more calls per day in very hot weather for cardiac arrest. There were 70 percent more calls for congestive heart failure. There were 345x more calls for heat exhaustion in hot weather and 19x more calls for dehydration.

#### Supporting code and output \[cq\]

``` r
# Select conditions
conditions <- c("Heat Exhaustion/Heat Stroke", "Dehydration","Respiratory Distress", "COPD (Emphysema/Chronic Bronchitis)", "End Stage Renal Disease", "Diabetic Hyperglycemia", "Diabetic Hypoglycemia", "Cardiac Arrest", "CHF (Congestive Heart Failure)")

# Calculate the total number of hours over the course of Summer 2018 that the heat index fell into each heat index level, as defined by the national weather service: not unsafe (under 80), caution (80-89), extreme caution (90-102), danger (103-124).   

heat_index_count_per_nws_five_scale_bucket <- dmh_ems %>%
  select(heat_index_nws_five_scale_bucket) %>%
  group_by(heat_index_nws_five_scale_bucket) %>%
  summarise(heat_index_count_per_nws_five_scale_bucket=n()) %>%
  arrange(heat_index_nws_five_scale_bucket)

# For each target condition, calculate the number of hours between calls at each temperature level.  This metric allows us to account for the fact that simply counting calls in each bucket would be flawed, because it wouldn't adjust for the rarity of very hot temperatures.

EMS_all %>%
  filter(primary_impression_group %in% conditions) %>%
  group_by(primary_impression_group, adjusted_heat_index_nws_five_scale_bucket) %>%
  summarise(condition_calls_count_per_bucket=n()) %>%
  inner_join(heat_index_count_per_nws_five_scale_bucket, by = c("adjusted_heat_index_nws_five_scale_bucket" = "heat_index_nws_five_scale_bucket")) %>%
  mutate(hours_per_call = heat_index_count_per_nws_five_scale_bucket/condition_calls_count_per_bucket) %>%
  select(primary_impression_group, adjusted_heat_index_nws_five_scale_bucket, hours_per_call) %>%
  tidyr::spread(adjusted_heat_index_nws_five_scale_bucket, hours_per_call) %>%
  select(primary_impression_group, `not_unsafe_under_80`,`danger_103_124`) %>%
  mutate(`calls_per_day_under_80` = 24/`not_unsafe_under_80`) %>%
  mutate(`calls_per_day_over_103` = 24/`danger_103_124`) %>%
  mutate(difference_day_percent = ((`calls_per_day_over_103`-`calls_per_day_under_80`)/`calls_per_day_under_80`))
```

    ## # A tibble: 9 x 6
    ## # Groups:   primary_impression_group [9]
    ##   primary_impress… not_unsafe_unde… danger_103_124 calls_per_day_u…
    ##   <chr>                       <dbl>          <dbl>            <dbl>
    ## 1 Cardiac Arrest               5.30           2.94            4.53 
    ## 2 CHF (Congestive…            15              8.83            1.6  
    ## 3 COPD (Emphysema…             5.61           3.31            4.28 
    ## 4 Dehydration                 41.7            2.21            0.575
    ## 5 Diabetic Hyperg…             7.33           5.3             3.28 
    ## 6 Diabetic Hypogl…             5.96           4.42            4.03 
    ## 7 End Stage Renal…           160             53               0.15 
    ## 8 Heat Exhaustion…           480              1.39            0.05 
    ## 9 Respiratory Dis…             3.34           2.79            7.18 
    ## # … with 2 more variables: calls_per_day_over_103 <dbl>,
    ## #   difference_day_percent <dbl>

### Fact: Hot neighborhoods have lower incomes \[cq\]

"The city’s hottest areas are poorer, which means the residents don’t have the resources to move out."

#### Explanation \[cq\]

In Baltimore's "community statistical areas", we examined the relationship between heat (mean afternoon temperature in our urban heat island data) and poverty. There were moderate correlations between poverty and heat (r =.4).

#### Supporting code and output \[cq\]

``` r
# Correlation coefficients
csa_tree_temp_demographics %>%
  select_if(is.numeric) %>%
  as.matrix() %>%
  correlate() %>%
  focus(matches("temp_")) %>%
  mutate(variable=rowname) %>%
  select(variable, temp_mean_aft) %>%
  filter(str_detect(variable, "family_households"))
```

    ## # A tibble: 1 x 2
    ##   variable                                                   temp_mean_aft
    ##   <chr>                                                              <dbl>
    ## 1 percent_of_family_households_living_below_the_poverty_line         0.398

### Fact: More affluent communities have more trees \[cq\]

"The streets have fewer trees than those in more affluent communities."

#### Explanation \[cq\]

In Baltimore "community statistical areas", there is a moderate negative correlation between an area's tree canopy cover and the area's poverty rate, with a correlation coefficient (r) of -.34. Generally, the poorer the area, the fewer trees it will have, and vice versa.

#### Supporting code and output \[cq\]

``` r
 csa_tree_temp_demographics %>%
  select_if(is.numeric) %>%
  as.matrix() %>%
  correlate() %>%
  focus(matches("15_lid_mean")) %>%
  mutate(variable=rowname) %>%
  select(variable, `15_lid_mean`) %>%
  filter(variable=="percent_of_family_households_living_below_the_poverty_line")
```

    ## # A tibble: 1 x 2
    ##   variable                                                   `15_lid_mean`
    ##   <chr>                                                              <dbl>
    ## 1 percent_of_family_households_living_below_the_poverty_line        -0.340

### Fact: Crime rates higher in poorer neighborhoods \[cq\]

"Crime rates are higher, so many people won’t put an air-conditioning unit in a first-floor window for fear of break-ins."

#### Explanation \[cq\]

In Baltimore "community statistical areas", there is a moderate positive correlation between an area's violent crime rate and the area's poverty rate, with a correlation coefficient (r) of .43, where 1 would reference a perfect positive correlation. Generally, the poorer the area, the more violent crime, and vice versa.

#### Supporting code and output \[cq\]

``` r
 csa_tree_temp_demographics %>%
  select_if(is.numeric) %>%
  as.matrix() %>%
  correlate() %>%
  focus(matches("percent_of_family_households_living_below_the_poverty_line")) %>%
  mutate(variable=rowname) %>%
  select(variable, percent_of_family_households_living_below_the_poverty_line) %>%
  filter(str_detect(variable, "violent")) %>%
  rename(poverty_rate = percent_of_family_households_living_below_the_poverty_line)
```

    ## # A tibble: 1 x 2
    ##   variable                               poverty_rate
    ##   <chr>                                         <dbl>
    ## 1 violent_crime_rate_per_1_000_residents        0.428

### Fact: Highest temperature, humidity sensor values \[cq\]

"Reporters from the University of Maryland’s Howard Center for Investigative Journalism and Capital News Service placed sensors that record heat and humidity inside several homes in McElderry Park and nearby neighborhoods. Those sensors recorded temperatures that reached as high as 97 degrees and heat index values of 119 degrees."

#### Explanation \[cq\]

In the homes referenced in this story where we placed sensors, the highest heat index reading we captured was 119 degrees, and the highest temperature reading was 96.8 degrees.

#### Supporting code and output \[cq\]

``` r
# bind together four sensor data sets
all_sensors_day_minute_averages <- bind_rows(michael_day_minute_averages, tammy_day_minute_averages, stephanie_day_minute_averages, audrey_day_minute_averages)

# return the highest temperature
all_sensors_day_minute_averages %>%
  filter(mean_indoor_temperature == max(mean_indoor_temperature)) %>%
  select(date_hour_minute, mean_indoor_temperature)
```

    ## # A tibble: 4 x 2
    ##   date_hour_minute    mean_indoor_temperature
    ##   <dttm>                                <dbl>
    ## 1 2019-07-19 20:55:00                    96.8
    ## 2 2019-07-19 21:06:00                    96.8
    ## 3 2019-07-19 21:30:00                    96.8
    ## 4 2019-07-19 21:45:00                    96.8

``` r
# return the highest heat index
all_sensors_day_minute_averages %>%
  filter(mean_indoor_heat_index == max(mean_indoor_heat_index)) %>%
  select(date_hour_minute, mean_indoor_heat_index)
```

    ## # A tibble: 1 x 2
    ##   date_hour_minute    mean_indoor_heat_index
    ##   <dttm>                               <dbl>
    ## 1 2019-07-20 18:12:00                    119

### Fact: Hotter inside than outside \[cq\]

"In some homes, those readings showed that it was hotter inside than outside. At 4 p.m. Saturday, July 20, the temperature in Baltimore hit 99 degrees F, but the humidity made it feel like 108 degrees F. Here is what the combination of heat and humidity felt like inside three East Baltimore rowhouses at 4 p.m. that day:

-   Michael Thomas and Alberta Wilkerson, second floor sensor. Temperature: 96. Relative humidity: 52%. What it felt like: 109.
-   Audrey DeWitt, first floor sensor. Temperature: 87. Relative humidity: 52%. What it felt like: 91.
-   Stephanie Pingley, second floor sensor. Temperature: 95. Relative humidity: 53%. What it felt like: 107."

#### Explanation \[cq\]

The outdoor heat, humidity and heat index were calculated using data from the Inner Harbor NWS monitoring station. Sensors we placed in their homes were used to calculate the indoor temperatures, heat index and humidity.

#### Supporting code and output \[cq\]

``` r
# temperature and heat index at 4 p.m. Saturday, July 20, 2019
dmh %>%
 filter(month == 7,
         year == 2019,
         day == 20,
         hour == 16) %>%
  select(date, hour, avg_hourly_temperature_dmh, avg_hourly_heat_index_dmh)
```

    ## # A tibble: 1 x 4
    ##   date        hour avg_hourly_temperature_dmh avg_hourly_heat_index_dmh
    ##   <date>     <dbl>                      <dbl>                     <dbl>
    ## 1 2019-07-20    16                         99                       108

``` r
# Michael and Alberta
michael_day_hourly_averages %>%
  mutate(date = date(date_hour)) %>%
  mutate(hour = hour(date_hour)) %>%
  filter(date == "2019-07-20") %>%
  filter(hour == 16) %>%
  select(date, hour, mean_indoor_temperature, mean_indoor_relative_humidity, mean_indoor_heat_index)
```

    ## # A tibble: 1 x 5
    ##   date        hour mean_indoor_tempe… mean_indoor_relati… mean_indoor_heat…
    ##   <date>     <int>              <dbl>               <dbl>             <dbl>
    ## 1 2019-07-20    16                 96                51.8              109.

``` r
# Audrey
audrey_day_hourly_averages %>%
  mutate(date = date(date_hour)) %>%
  mutate(hour = hour(date_hour)) %>%
  filter(date == "2019-07-20") %>%
  filter(hour == 16) %>%
  select(date, hour, mean_indoor_temperature, mean_indoor_relative_humidity, mean_indoor_heat_index)
```

    ## # A tibble: 1 x 5
    ##   date        hour mean_indoor_tempe… mean_indoor_relati… mean_indoor_heat…
    ##   <date>     <int>              <dbl>               <dbl>             <dbl>
    ## 1 2019-07-20    16               87.4                  52                91

``` r
# Stephanie
stephanie_day_hourly_averages %>%
  mutate(date = date(date_hour)) %>%
  mutate(hour = hour(date_hour)) %>%
  filter(date == "2019-07-20") %>%
  filter(hour == 16) %>%
  select(date, hour, mean_indoor_temperature, mean_indoor_relative_humidity, mean_indoor_heat_index)
```

    ## # A tibble: 1 x 5
    ##   date        hour mean_indoor_tempe… mean_indoor_relati… mean_indoor_heat…
    ##   <date>     <int>              <dbl>               <dbl>             <dbl>
    ## 1 2019-07-20    16               94.8                  53              107.

### Fact: Tammy Jackson's house on July 21 \[cq\]

"On the first floor of Jackson’s two-story rowhouse, the heat index registered 93 degrees at 10 p.m. on Sunday, July 21. Outside, the heat index was 9 degrees lower, 84 degrees."

#### Explanation \[cq\]

The following code shows the values presented in the sentence above.

#### Supporting code and output \[cq\]

``` r
tammy_day_hourly_averages %>%
  mutate(date = date(date_hour)) %>%
  mutate(hour = hour(date_hour)) %>%
  filter(date == "2019-07-21") %>%
  filter(hour == 22) %>%
  select(date_hour, mean_indoor_heat_index, mean_outdoor_heat_index, indoor_heat_index_difference)
```

    ## # A tibble: 1 x 4
    ##   date_hour           mean_indoor_heat… mean_outdoor_hea… indoor_heat_inde…
    ##   <dttm>                          <dbl>             <dbl>             <dbl>
    ## 1 2019-07-21 22:00:00                93                84                 9

### Fact: Hotter inside Stephanie Pingley's house than outside \[cq\]

"A sensor inside a bedroom showed that the heat index during the heat wave was consistently higher inside than outside Pingley’s house."

#### Explanation \[cq\]

Between July 16 and July 23, the heat index inside of Pingley's house was higher than the outside for more hours (108) than hours when the opposite was true (60).

#### Supporting code and output \[cq\]

``` r
stephanie_day_hourly_averages %>%
  filter(date_hour >= "2019-07-16",
         date_hour < "2019-07-23") %>%
  mutate(difference = case_when(
      indoor_heat_index_difference > 0 ~ "hours hotter inside",
      indoor_heat_index_difference <= 0 ~ "hours hotter outside"
  )) %>%
  group_by(difference) %>%
  summarise(count=n())
```

    ## # A tibble: 2 x 2
    ##   difference           count
    ##   <chr>                <int>
    ## 1 hours hotter inside    108
    ## 2 hours hotter outside    60

### Fact: Hottest seven-day stretch of the summer \[cq\]

"The seven-day stretch between July 16 and July 22 were the hottest consecutive days of the summer."

#### Explanation \[cq\]

The average temperature between July 16 and July 22 was 94.2 degrees, hotter than any period of the summer so far.

#### Supporting code and output \[cq\]

``` r
dmh %>%
  filter(year == 2019) %>%
  filter(date >= "2019-06-21",
         date <= "2019-09-21")
```

    ## # A tibble: 1,749 x 9
    ##    date        year month   day  hour avg_hourly_temp… avg_hourly_dewp…
    ##    <date>     <dbl> <dbl> <dbl> <dbl>            <dbl>            <dbl>
    ##  1 2019-06-21  2019     6    21     0             73               70  
    ##  2 2019-06-21  2019     6    21     1             73               70  
    ##  3 2019-06-21  2019     6    21     2             73               69.1
    ##  4 2019-06-21  2019     6    21     3             73.9             64  
    ##  5 2019-06-21  2019     6    21     4             73.9             62.1
    ##  6 2019-06-21  2019     6    21     5             73               62.1
    ##  7 2019-06-21  2019     6    21     6             73.9             62.1
    ##  8 2019-06-21  2019     6    21     7             73.9             60.1
    ##  9 2019-06-21  2019     6    21     8             73.9             60.1
    ## 10 2019-06-21  2019     6    21     9             73.9             60.1
    ## # … with 1,739 more rows, and 2 more variables:
    ## #   avg_hourly_relative_humidity_dmh <dbl>,
    ## #   avg_hourly_heat_index_dmh <dbl>

``` r
# compute means for the summer
summer_means <- dmh %>%
  filter(year == 2019) %>%
  filter(date >= "2019-06-21",
         date <= "2019-09-21") %>%
  group_by(`date`) %>%
  summarise(min_temp = min(avg_hourly_temperature_dmh),
            max_temp = max(avg_hourly_temperature_dmh),
            mean_temp = mean(avg_hourly_temperature_dmh),
            min_heat_index = min(avg_hourly_heat_index_dmh),
            max_heat_index = max(avg_hourly_heat_index_dmh),
            mean_heat_index = mean(avg_hourly_heat_index_dmh)
  )

# calculate mean temperature for seven days prior in each date in data
running_average <- as_tibble(runMean(summer_means$mean_heat_index, n=7))

# bind moving average back to summer means
summer_means <- bind_cols(summer_means, running_average) %>%
  select(date, value) %>%
  rename(seven_day_prior_mean_temp = value) %>%
  arrange(desc(seven_day_prior_mean_temp))

# display summer means
summer_means
```

    ## # A tibble: 73 x 2
    ##    date       seven_day_prior_mean_temp
    ##    <date>                         <dbl>
    ##  1 2019-07-22                      94.2
    ##  2 2019-07-21                      93.5
    ##  3 2019-07-23                      91.9
    ##  4 2019-07-20                      91.8
    ##  5 2019-07-24                      89.9
    ##  6 2019-07-19                      89.5
    ##  7 2019-07-25                      88.0
    ##  8 2019-08-22                      87.6
    ##  9 2019-07-18                      87.5
    ## 10 2019-08-21                      86.9
    ## # … with 63 more rows

### Fact: Heat index on July 21 \[cq\]

"The heat index reached 111 degrees at 4 p.m. July 21."

#### Explanation \[cq\]

The heat index reached 111 degrees at 4 p.m. July 21.

#### Supporting code and output \[cq\]

``` r
dmh %>%
  filter(date == "2019-07-21") %>%
  filter(hour == 16) %>%
  select(date, hour, avg_hourly_heat_index_dmh)
```

    ## # A tibble: 1 x 3
    ##   date        hour avg_hourly_heat_index_dmh
    ##   <date>     <dbl>                     <dbl>
    ## 1 2019-07-21    16                       111

### Fact: Heat index in the bedroom \[cq\]

"The heat index reached 113 degrees at 8 p.m. on July 19; it averaged 98 degrees during the seven-day period."

#### Explanation \[cq\]

The heat index reached 113 degrees at 8 p.m. on July 19. The mean indoor heat index was 98 degrees during that period.

#### Supporting code and output \[cq\]

``` r
# Stephanie heat index on July 19
stephanie_day_hourly_averages %>%
  mutate(date = date(date_hour)) %>%
  mutate(hour = hour(date_hour)) %>%
  filter(date == "2019-07-19") %>%
  filter(hour == 20) %>%
  select(date_hour, mean_indoor_heat_index)
```

    ## # A tibble: 1 x 2
    ##   date_hour           mean_indoor_heat_index
    ##   <dttm>                               <dbl>
    ## 1 2019-07-19 20:00:00                   113.

``` r
# Average indoor heat index during seven day period
stephanie_day_hourly_averages %>%
  mutate(date = date(date_hour)) %>%
  filter(date >= "2019-07-16") %>%
  filter(date <= "2019-07-22") %>%
  summarise(mean_indoor_heat_index = mean(mean_indoor_heat_index))
```

    ## # A tibble: 1 x 1
    ##   mean_indoor_heat_index
    ##                    <dbl>
    ## 1                   98.2

### Fact: Minimum heat index in Pingley bedroom \[cq\]

"The average hourly heat index in the bedroom never dropped below 89 degrees."

#### Explanation \[cq\]

The lowest average hourly heat index in the bedroom during that period was 88.8 degrees, or 89 rounded.

#### Supporting code and output \[cq\]

``` r
stephanie_day_hourly_averages %>%
  mutate(date = date(date_hour)) %>%
  filter(date >= "2019-07-16") %>%
  filter(date <= "2019-07-22") %>%
  summarise(min_indoor_heat_index = min(mean_indoor_heat_index))
```

    ## # A tibble: 1 x 1
    ##   min_indoor_heat_index
    ##                   <dbl>
    ## 1                  88.8

### Fact: Heat index indoors and out \[cq\]

"The heat index was consistently higher inside Pingley’s home than it was outside."

#### Explanation \[cq\]

During that week period, there were 108 hours when the heat index inside was higher than the outside heat index, and only 60 hours when the opposite was true.

#### Supporting code and output \[cq\]

``` r
stephanie_day_hourly_averages %>%
  filter(date_hour >= "2019-07-16",
         date_hour < "2019-07-23") %>%
  mutate(difference = case_when(
      indoor_heat_index_difference > 0 ~ "hours hotter inside",
      indoor_heat_index_difference <= 0 ~ "hours hotter outside"
  )) %>%
  group_by(difference) %>%
  summarise(count=n())
```

    ## # A tibble: 2 x 2
    ##   difference           count
    ##   <chr>                <int>
    ## 1 hours hotter inside    108
    ## 2 hours hotter outside    60

### Fact: Outdoor heat index on July 19

"At 8 p.m. July 19, in the midst of the summer's most brutal heat wave, the outdoor heat index hit 102 degrees."

#### Explanation \[cq\]

The heat index in Baltimore hit 102 degrees at 8 p.m. on July 19.

#### Supporting code and output \[cq\]

``` r
dmh %>%
  filter(date == "2019-07-19") %>%
  filter(hour == 20) %>%
  select(date, hour, avg_hourly_heat_index_dmh)
```

    ## # A tibble: 1 x 3
    ##   date        hour avg_hourly_heat_index_dmh
    ##   <date>     <dbl>                     <dbl>
    ## 1 2019-07-19    20                       102

### Fact: Indoor heat index on July 19 \[cq\]

"Inside Pingley’s house, it was 11 degrees hotter, with a heat index of 113 degrees."

#### Explanation \[cq\]

At 8 p.m. on July 19, the heat index indoors was 112.7 degrees inside, and the outdoor heat index was 102 degrees, with a difference of 10.7 degrees.

#### Supporting code and output \[cq\]

``` r
stephanie_day_hourly_averages %>%
  mutate(date = date(date_hour)) %>%
  mutate(hour = hour(date_hour)) %>%
  filter(date == "2019-07-19") %>%
  filter(hour ==  20) %>%
  select(date_hour, mean_indoor_heat_index, mean_outdoor_heat_index,indoor_heat_index_difference)
```

    ## # A tibble: 1 x 4
    ##   date_hour           mean_indoor_heat… mean_outdoor_hea… indoor_heat_inde…
    ##   <dttm>                          <dbl>             <dbl>             <dbl>
    ## 1 2019-07-19 20:00:00              113.               102              10.7

### Fact: Heat index Baltimore July 20 \[cq\]

"At 4 a.m. July 20, the heat index in Baltimore was still 89 degrees."

#### Explanation \[cq\]

At 4 a.m. July 20, the heat index in Baltimore was still 89 degrees.

#### Supporting code and output \[cq\]

``` r
dmh %>%
  filter(date == "2019-07-20") %>%
  filter(hour == 4) %>%
  select(date, hour, avg_hourly_heat_index_dmh)
```

    ## # A tibble: 1 x 3
    ##   date        hour avg_hourly_heat_index_dmh
    ##   <date>     <dbl>                     <dbl>
    ## 1 2019-07-20     4                        89

### Fact: Heat index in Pingley's house July 20 \[cq\]

"Inside Pingley’s house, in the bedroom where two children sleep, it felt even hotter, with a heat index of 99 degrees."

#### Explanation \[cq\]

The heat index in Pingley's house at 4 a.m. July 20 was 99.3 degrees.

#### Supporting code and output \[cq\]

``` r
stephanie_day_hourly_averages %>%
  mutate(date = date(date_hour)) %>%
  mutate(hour = hour(date_hour)) %>%
  filter(date == "2019-07-20") %>%
  filter(hour ==  4) %>%
  select(date_hour, mean_indoor_heat_index)
```

    ## # A tibble: 1 x 2
    ##   date_hour           mean_indoor_heat_index
    ##   <dttm>                               <dbl>
    ## 1 2019-07-20 04:00:00                   99.3

### Fact: Heat index Michael Thomas and Alberta Wilkerson \[cq\]

"By Saturday, the heat index inside the second-floor apartment of Michael Thomas and Alberta Wilkerson hit 112 degrees. A fan pushed hot air around. Thomas, 61, has emphysema. Wilkerson, 49, has had a heart attack."

#### Explanation \[cq\]

On Saturday, July 20, the heat index in their apartment hit 111.8 degrees.

#### Supporting code and output \[cq\]

``` r
michael_day_hourly_averages %>%
  mutate(date = date(date_hour)) %>%
  mutate(hour = hour(date_hour)) %>%
  filter(date == "2019-07-20") %>%
  arrange(desc(mean_indoor_heat_index)) %>%
  select(date_hour, mean_indoor_heat_index)
```

    ## # A tibble: 17 x 2
    ##    date_hour           mean_indoor_heat_index
    ##    <dttm>                               <dbl>
    ##  1 2019-07-20 03:00:00                   112.
    ##  2 2019-07-20 05:00:00                   112.
    ##  3 2019-07-20 04:00:00                   112.
    ##  4 2019-07-20 02:00:00                   111 
    ##  5 2019-07-20 01:00:00                   111.
    ##  6 2019-07-20 00:00:00                   110.
    ##  7 2019-07-20 15:00:00                   110.
    ##  8 2019-07-20 06:00:00                   109.
    ##  9 2019-07-20 16:00:00                   109.
    ## 10 2019-07-20 14:00:00                   109.
    ## 11 2019-07-20 13:00:00                   108.
    ## 12 2019-07-20 12:00:00                   108.
    ## 13 2019-07-20 07:00:00                   107.
    ## 14 2019-07-20 11:00:00                   107.
    ## 15 2019-07-20 10:00:00                   106 
    ## 16 2019-07-20 08:00:00                   106.
    ## 17 2019-07-20 09:00:00                   106.

#### Fact: Historical heat index days

"Historically, the Baltimore area has averaged about six days a year when the heat index exceeded 100 degrees, according to new research from the Union of Concerned Scientists and the University of Idaho. If no action is taken to reduce carbon emissions, by mid-century that figure will rise to more than 37 days annually, according to the researchers. The study defines mid-century as starting in 17 years. By the end of the century, as a baby born today becomes a senior citizen, there will be 65 days with a heat index of 100 degrees or higher, the researchers projected. That’s about the same number as McAllen, Texas, a city that abuts the Mexican border."

#### Explanation \[cq\]

The Union of Concerned Scientists \[Killer Heat in the United States\] \[study\](<https://www.ucsusa.org/sites/default/files/attach/2019/07/killer-heat-analysis-full-report.pdf>) released this summer included detailed tables projecting the number of days of 100+ heat index days for most U.S. cities, and projected how many additional days of 100+ heat index days there would be by mid-century. They found there were six days of 100+ heat index days per year historically in Baltimore, and by mid-century there would be 37 days. By end of the century, there would 65, about as many as McAllen, Texas has today (67). Note: our own analysis of historical Baltimore heat index data at a NWS Inner Harbor monitoring station found that the 6 days per year figure was likely a conservative estimate.

#### Supporting code and output \[cq\]

``` r
heat_index_projections %>%
  select(state, city, historical_100_plus, midcentury_no_action_100_plus, endcentury_no_action_100_plus) %>%
  filter((state == "MD" | state == "TX"), (city == "Baltimore" | city == "McAllen"))
```

    ## # A tibble: 2 x 5
    ##   state city    historical_100_p… midcentury_no_actio… endcentury_no_actio…
    ##   <chr> <chr>               <dbl>                <dbl>                <dbl>
    ## 1 MD    Baltim…                 6                   37                   65
    ## 2 TX    McAllen                67                  137                  164

### Fact: tree canopy on McElderry Park neighborhood \[cq\]

"Photo caption: This block at the edge of the city's McElderry Park neighborhood had tree canopy coverage of about 8% in 2015."

#### Explanation \[cq\]

The block in the photo is on North Milton and East Monument at the edge of the McElderry Park neighborhood. The street shown is split between two U.S. Census blocks, with IDs of "245100702004002" and "245100702004002". They had 7.6 percent and 8.7 percent tree canopy cover in 2015.

#### Supporting code \[cq\]

``` r
blocks_tree_temp_demographics %>%
  filter(geoid10 == "245100702004002" | geoid10 == "245100702005005") %>%
  select(geoid10, `15_lid_mean`)
```

    ## # A tibble: 2 x 2
    ##   geoid10 `15_lid_mean`
    ##     <dbl>         <dbl>
    ## 1 2.45e14        0.0869
    ## 2 2.45e14        0.0757

### Fact: East Baltimore Tree Cover \[cq\]

"And in 2015, many East Baltimore neighborhoods had a tree canopy of about 10%, according to a Howard Center analysis of tree canopy data gathered by researchers at the U.S. Forest Service and the University of Vermont Spatial Analysis Lab."

#### Explanation \[cq\]

The code below shows the percent of tree canopy cover in more than a dozen east Baltimore neighborhoods in 2015. The range is from 4 to 14.

#### Supporting code and output \[cq\]

``` r
east_baltimore_nsas <- c("Berea", "Broadway East", "Oliver", "Middle East",
                 "Biddle Street","Milton-Montford", "Madison-Eastend",
                 "CARE", "McElderry Park", "Ellwood Park/Monument",
                 "Patterson Place", "Patterson Park Neighborhood",
                 "Baltimore Highlands", "Highlandtown",
                 "Upper Fells Point") %>%
  lapply(tolower)

nsa_tree_temp %>%
  filter(nsa_name %in% east_baltimore_nsas) %>%
  select(nsa_name, `15_lid_mean`) %>%
  arrange(`15_lid_mean`) %>%
  mutate(`15_lid_mean_percentage` = 100*(`15_lid_mean`)) %>%
  select(nsa_name, `15_lid_mean_percentage`)
```

    ## # A tibble: 15 x 2
    ##    nsa_name                    `15_lid_mean_percentage`
    ##    <chr>                                          <dbl>
    ##  1 patterson park neighborhood                     4.19
    ##  2 highlandtown                                    4.26
    ##  3 berea                                           5.97
    ##  4 mcelderry park                                  6.14
    ##  5 milton-montford                                 6.41
    ##  6 ellwood park/monument                           6.45
    ##  7 middle east                                     6.76
    ##  8 patterson place                                 7.46
    ##  9 care                                            7.49
    ## 10 madison-eastend                                 7.71
    ## 11 baltimore highlands                             7.86
    ## 12 broadway east                                  10.6 
    ## 13 upper fells point                              11.2 
    ## 14 biddle street                                  12.7 
    ## 15 oliver                                         13.9
