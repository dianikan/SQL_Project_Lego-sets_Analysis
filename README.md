# LEGO Sets Analysis

This project explores a dataset of LEGO sets, analyzing various aspects of LEGO's production history and trends. The analysis focuses on answering key questions about LEGO sets released since 1970.

## Project Goals

The primary goals of this project are to:

* Determine the total number of LEGO sets released since 1970 and identify any noticeable trends in production.
* Investigate the relationship between the price of a LEGO set and its number of pieces.
* Identify the most popular LEGO theme in each decade.
* Examine the correlation between LEGO minifigures and licensed sets.
* Identify LEGO themes that have been reintroduced after a period of discontinuation.

## Dataset

The dataset used in this analysis contains information about LEGO sets, including:

* `set_id`
* `name`
* `year`
* `theme`
* `subtheme`
* `themeGroup`
* `category`
* `pieces`
* `minifigs`
* `agerange_min`
* `US_retailPrice`
* `bricksetURL`
* `thumbnailURL`
* `imageURL`

## Analysis and Queries

### 1. How many LEGO sets have been released since 1970? Is there a noticeable trend?

```sql
use lego_sets;
select count(distinct set_id) from lego_sets;
select count(*) as lego_set, year from lego_sets group by year order by year;
![LEGO Sets by Year](images/lego_sets_by_year.png)

This chart shows the number of Lego sets that were released each year.
