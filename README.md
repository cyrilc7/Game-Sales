# Game Sales Analysis - A Data Analysis Project

## Table of Contents

 * [Project Overview](#project-overview)
 * [Data Sources](#data-sources)
 * [Tools](#tools)
 * [Analysis TOC](#analysis-toc)
 * [Process of Analysis](#process-of-analysis)
 * [Results and Findings](#results-and-findings)
 * [Limitations](#limitations)
 * [Go Further](#go-further)

## Project Overview

This data analysis project aims to provide insights into the video games industry from 1980 to 2020. By analyzing various aspects of the markets over different regions of the world, we seek to identify trends, make data-driven recommendations and gain an overall deeper understanding of the industry.

## Data Sources

The primary dataset used for this analysis is the "vgsales.csv" file presenting detailed information about a list of video games with sales greater than 100,000 copies. The dataset was obtained from [this website](https://zenodo.org/records/5898311#.Y9Y2K9JBwUE).

## Tools

Data Processing / Data Analysis / Data Visualization: ***Python***

## Analysis TOC:

**Data Preparation**

    Loading Libraries
    Loding Data
    Data Preprocessing

**Market Analysis**

    I. Best selling video games
    II. Platforms Analysis
        1. By Number of Games Released
        2. By Sales
    III. Genre Analysis
        1. Popular Game Genres
        2. Evolution of Game Genres from 1980 to 2020
    IV. Publishers Analysis
        1. Most Productive Publisher
        2. Best Selling Publishers
        3. Nintendo - More numbers
            *Most selling games*
            *Most selling genres*
            *Number of Games released*
                a. By Genre
                b. By Platform
        4. Electronic Arts - More numbers
            *Most selling games*
            *Most selling genres*
            *Number of Games released*
                a. By Genre
                b. By Platform
        5. Activision - More numbers
            *Most selling games*
            *Most selling genres*
            *Number of Games released*
                a. By Genre
                b. By Platform
**Conclusion**

    I. The video games market
    II. Case use
        a. As a developer
        b. As a company

## Process of Analysis

### Data Preparation

In the initial data preparation phase, we performed the following tasks:
   * Data loading and inspection 
   * Handling missing values
   * Data preprocessing
   * Checking for outliers

### Exploratory Data Analysis (EDA)

During the EDA phase, we answered key questions such as:
   * What is the overall trend of the industry?
   * Are there any differences between different geographical markets?
   * How did the industry evolve over time?
   * Which games are top sellers?
   * Which platform sells best overall and in different regions?
   * Which genre sells best overall and in different regions?
   * Who is the most productive publisher?
   * Which publisher sells best overall and in different regions?
   * What is the strategy of the main competitors in the industry?

### Data Analysis and Visualization

For Data Analysis and Visualization, we used the following Python libraries:
   * Pandas
   * Numpy
   * MatPlotLib
   * Seaborn

Some of the techniques used include:

``` python
# type conversion
df['Year']= df['Year'].astype(int)

# data processing
df = df.dropna()
df.isna().sum()

# dataframe inspection
df.describe()
df.head()
df.tail()

# using boxplots to check for outliers
sns.boxplot(x=sales_df['Global_Sales'])

# creating and modifying different parameters of barplots / subplots / lineplots for visualization 
sns.barplot(x='', y='', hue='', data='', palette='')
plt.xlabel('')
plt.ylabel('')
plt.title('')
plt.show()
```

## Results and Findings

### *Results*
The analysis results are summarized as follows:
   * The video game's industry from 1980 to 2020 has seen numbers and numbers of new games on many platforms. Most didn't sell but the top percentiles performed extremely well
   * North America (NA) is the biggest market for this industry by far, followed by Europe, Japan and then the rest of the world
   * NA,EU and Other regions show similar patterns. However, Japan shows significantly different results
   * The most selling platforms are the PS Series, the X360, the Wii and the DS
   * Action games and Sports games have been the most prolific genres since 1980. Role-Playing games perform surprisingly well in Japan and Shooter sell great everywhere else
   * The video game's industry is led by a clear top 3:
        * Nintendo: focuses more on quality than quantity (releases much less games than its competitors) and gets most of its profit from older games (before 2010)
        * EA and Activision: release a lot of games, get astonishing market shares anywhere except in Japan. EA focuses on Sports games while Activision focuses on Shooter Games

### *Recommendations
You can get many insights from this analysis if you are a company or a developer. If you are a developer, we recommend to focus on:
   * Recent versions of the PlayStation series, the XBox Series, or the Nintendo consoles
   * Action and Sports games if you plan on targetting all regions, or releasing high-performing niches (Role-Playing games in Japan or Shooter games everywhere else)
   * Approach any of the "Big 3" depending on the market and genre that you are targetting:
        * Nintendo for Role-Playing games and/or Japanese Market
        * EA for a more global approach and if you plan to make a Sports game
        * Activision if your strategy is to create a Shooter game.

## Limitations

I had to remove all missing values from year column, which can slightly affect the accuracy of the analysis. Also, the dataset goes until 2020, and thus does not include Covid period where the market has probably changed due to staying in.
However, the dataset and the analysis still managed to achieved its goal of observing patterns in the market.

## Go Further

One interesting ideas to complete the analysis of the industry would be to perform an analysis on the impact of the Corona on the video games market.