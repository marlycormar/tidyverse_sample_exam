---
title: "Sample Exam"
output:
  html_document:
    keep_md: true
    toc: true
    toc_float: true
    theme: simplex
    highlight: tango
---





<!---------------------------------------------------------------------------->
<!--------------------------- INSTRUCTIONS
<!---------------------------------------------------------------------------->

## Instructions
1. This exam covers material from R for Data Science (https://r4ds.had.co.nz/). If you have any questions about scope, please get in touch - we'd be happy to clarify.
2. You may use any books or online resources you want during this examination, but you may not communicate with any person other than your examiner.
3. You are required to use the RStudio IDE for this exam. You may use either the desktop edition or rstudio.cloud as you prefer.
4. You may do your work in an R script or an R Markdown file, and may use one for the whole exam or one for each question as your prefer. Whichever you choose, you must send your final work to the examiner by email upon completion of the examination.
5. Please let the examiner know when you finish each part of each question so that they can check your work.

<!---------------------------------------------------------------------------->
<!--------------------------- QUESTION 1
<!---------------------------------------------------------------------------->

## Question 1

The file [at_health_facilities.csv](https://education.rstudio.com/blog/2020/02/instructor-certification-exams/at_health_facilities.csv) contains a tidy dataset with four columns:

- The ISO3 code of the country that reported data.
- The year for which data was reported. 
- The percentage of HIV-positive children born to HIV-positive mothers age 15–17. 
- The percentage of HIV-positive children born to HIV-positive mothers age 20–34.

Please answer the following questions:

1. How many countries reported data?
2. What is the difference between the minimum and maximum year with valid data for each country?
3. How many countries reported data in 3 or more years?
4. Which countries reported 100% incidence for at least one year in either age group?


<!---------------------------------------------------------------------------->
<!--------------------------- QUESTION 2
<!---------------------------------------------------------------------------->

## Question 2

A student has sent you the file [rmd-country-profile.Rmd](https://education.rstudio.com/blog/2020-01-20-instructor-certification-exams/rmd-country-profile.Rmd), which is an R Markdown document analyzing the data in [at_health_facilities.csv](https://education.rstudio.com/blog/2020/02/instructor-certification-exams/at_health_facilities.csv) for Bangladesh. They could not knit the file, and are providing you with the raw .Rmd file instead of a rendered file.

1. Go through the file, fixing things that are preventing it from knitting cleanly.
2. Change the two lines of bold text to H2-level headers to organize the document, and add a table of contents.
3. Convert this R Markdown report for Bangladesh into a parameterized report with the country's iso3 code as its parameter. Knit a new country profile for Egypt (ISO3 code "EGY").


<!---------------------------------------------------------------------------->
<!--------------------------- QUESTION 3
<!---------------------------------------------------------------------------->

## Question 3

You have been given a CSV file [infant_hiv.csv](https://education.rstudio.com/blog/2020/02/instructor-certification-exams/infant_hiv.csv) that is formatted as follows:

- The first column is ISO3 country codes.
- There are three columns for each year from 2009 to 2017. Each set has estimated, low, and high values for the year (in that order).
- A dash `-` indicates that no data is available.
- Our analyst tells us that `>95%` means "the data is unreliable".

Your task is to turn this into a tidy data table for further analysis:

1. Describe what columns a tidy layout for this data would have and why.
2. Write a function that takes the name of a file containing this table as input and returns a tidy version of the table.
    - The function should replace all `-` and `>95%` values with `NA`.
    - The body of the function may contain one or more pipelines and may create temporary or intermediate variables, but may not contain any loops.


<!---------------------------------------------------------------------------->
<!--------------------------- QUESTION 4
<!---------------------------------------------------------------------------->

## Question 4

The file [ranking.csv](https://education.rstudio.com/blog/2020/02/instructor-certification-exams/ranking.csv) contains two columns:

- The ID of an item being rated.
- A rating, which is one of "negative", "positive", "indifferent", or "wtf" (meaning the respondent didn't understand the question).

There are multiple ratings for each item. The plot below shows this data:

- Each dot represents one item i.
- The size of the circles shows the total number of ratings for item i.
- The X coordinate for item i is the percentage of ratings for that item that are "negative".
- The Y coordinate for item i is the percentage of ratings for that item that are "positive".
- The regression line is created using the 'lm' method.


![](../images/ranking-scatterplot-1.png)

Re-create this plot using the tidyverse and ggplot2, fixing any mistakes you notice along the way.