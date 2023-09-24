# Bellabeat Smart Device Usage Analysis
## Description
Bellabeat is a high-tech company that manufactures health-focused smart products for women. This project aims to analyze consumers’ usage of non-Bellabeat smart devices and apply those insights to recommend marketing strategies to Bellabeat. Every aspect of this project is a sample code which shows how to do the following:

* Investigate each table to look for possible outliers
* Check for data consistency and comprehensiveness
* Data Manipulation
* Data Visualization

For full documentation, view [here](https://seeying147.github.io/Bellabeat-Analysis/).

## Dataset
The dataset was obtained from the online data science platform Kaggle titled “[FitBit Fitness Tracker Data](https://www.kaggle.com/datasets/arashnic/fitbit)". It contains personal fitness tracker data from 30 fitbit users between 03/12/2016 and 05/12/2016. The original dataset is organized in 18 separate .csv files but we will only use the following 7 .csv files for analysis:

* dailyActivity_merged.csv
* heartrate_seconds_merged.csv
* hourlyCalories_merged.csv
* hourlyIntensities_merged.csv
* hourlySteps_merged.csv
* sleepDay_merge.csv
* weigthLog_Info_merged.csv

## Technologies Used 
The project is created with:
* mySQL v8.0.33 (Install [here](https://dev.mysql.com/downloads/installer/))
* RStudio v4.1.2 (Install [here](https://posit.co/products/open-source/rstudio/))

## Setup
To run this project:
* Open mySQL. In MySQL workbench, click on the schema logo to create a new schema "fitbit".
* Run all queries in sqldata file to import the above 7 .csv files into "fitbit" schema.
* Download index.Rmd and open the R Markdown document in RStudio.
* In R studio, install the following packages using the following code:
```{r}
install.packages(RMariaDB)
install.packages(dplyr)
install.packages(ggplot2)
install.packages(tidyverse)
install.packages(lubridate)
install.packages(scales)
install.packages(gridExtra)
```
* In index.Rmd, under the section "Dealing with DATETIME column", user has to connect to their SQL database to run SQL query in RStudio. Edit the SQL connection code such that the it is in the following format:
```{r}
#Run the following code to connect to MySQL database
library(RMariaDB)
con <- dbConnect(MariaDB(),
                 user = "Insert user name which you indicate when installing mySQL",
                 password = "Insert your password",
                 dbname = "fitbit",
                 host = "Insert your host name",
                 port = 3306)
```
* Click "Knit" to view the project.

## License
This project is licensed under MIT License- see LICENSE file for details
