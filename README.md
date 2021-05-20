# Nestor_Leon_Portfolio
Nestor Leon Jr's Official Data Analytics Portfolio
Project 1: Happiness Score and Gdp Per Capita
---
title: "Portfolio Project"
author: "Nestor Leon Jr."
date: "5/19/2021"
output: html_document
---

## Project 1: World Happiness Score Project

Is happiness correlated to a persons living standards and productivity? I posed this question as a way to answer a series of questions that attribute to why people in various countries would be happy or not? The first of which being, is GDP per Capita correlated with a happiness score? More importantly does a higher gdp per capita score lead to a higher happiness score? As well as does a lower gdp per capita equal to a lower happiness score?

```{r visualization of happiness score and gdp per capita}
library(ggplot2)
`2019_happiness_project` <- read.csv("2019_happiness_project.csv")
summary(`2019_happiness_project`)
```

```{r visualizations of happiness_score and gdp_per_capita}
ggplot(data = `2019_happiness_project`) +
  geom_point(aes(x=happiness_score,y=gdp_per_capita)) +
  geom_smooth(method = "lm",aes(x=happiness_score,y=gdp_per_capita))
```

Based on my findings there is a positive correlation between the GDP per Capita of countries and their Happiness Score. Therefore, the higher the GDP per Capita the higher the Happiness Score would be as well as the lower the Gdp per Capita score the lower the countries happiness score will be, based on this graph.
