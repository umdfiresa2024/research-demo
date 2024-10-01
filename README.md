# Research Question


Step 1. Install necessary packages.

``` r
install.packages("tidyverse")
```

    Installing package into '/cloud/lib/x86_64-pc-linux-gnu-library/4.4'
    (as 'lib' is unspecified)

``` r
install.packages("kableExtra")
```

    Installing package into '/cloud/lib/x86_64-pc-linux-gnu-library/4.4'
    (as 'lib' is unspecified)

Step 2. Declare that you will use these packages in this session.

``` r
library("tidyverse")
```

    ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
    ✔ dplyr     1.1.4     ✔ readr     2.1.5
    ✔ forcats   1.0.0     ✔ stringr   1.5.1
    ✔ ggplot2   3.5.1     ✔ tibble    3.2.1
    ✔ lubridate 1.9.3     ✔ tidyr     1.3.1
    ✔ purrr     1.0.2     
    ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ✖ dplyr::filter() masks stats::filter()
    ✖ dplyr::lag()    masks stats::lag()
    ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors

``` r
library("kableExtra")
```


    Attaching package: 'kableExtra'

    The following object is masked from 'package:dplyr':

        group_rows

Step 3. Upload the dataframe that you have created in Spring 2024 into
the repository.

Step 4. Open the dataframe into the RStudio Environment.

``` r
df<-read.csv("data.csv")
```

Step 5. Use the **head** and **kable** function showcase the first 10
rows of the dataframe to the reader.

``` r
kable(head(df))
```

| fips | year | smm | nox_emit | so2_emit | co2_emit | nbp | state | pop_all | dptp_xtile_1 | dptp_xtile_2 | dptp_xtile_4 | dptp_xtile_5 | dptp_xtile_6 | dptp_xtile_7 | dptp_xtile_8 | dptp_xtile_9 | dptp_xtile_10 | dptp_xtile_11 | dptp_xtile_12 | dptp_xtile_13 | dptp_xtile_14 | dptp_xtile_15 | dptp_xtile_16 | dptp_xtile_17 | dptp_xtile_18 | dptp_xtile_19 | dptp_xtile_20 | tmean_xtile_1 | tmean_xtile_2 | tmean_xtile_4 | tmean_xtile_5 | tmean_xtile_6 | tmean_xtile_7 | tmean_xtile_8 | tmean_xtile_9 | tmean_xtile_10 | tmean_xtile_11 | tmean_xtile_12 | tmean_xtile_13 | tmean_xtile_14 | tmean_xtile_15 | tmean_xtile_16 | tmean_xtile_17 | tmean_xtile_18 | tmean_xtile_19 | tmean_xtile_20 | mean_prcp | n |
|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 1001 | 1999 | 1 | 0.0000000 | 0.0000000 | 0.00000 | 1 | 1 | 42963 | 0.000000 | 0.000000 | 0.000000 | 0.000000 | 0.000000 | 0.000000 | 0.000000 | 2.000000 | 5.000000 | 4.000000 | 2.000000 | 6.000000 | 8.000000 | 10.000001 | 12.000000 | 14.000000 | 20.000002 | 24.000000 | 46.000000 | 0.0000000 | 0.0000000 | 0.000000 | 0.000000 | 0.000000 | 0.00000 | 0.000000 | 0.000000 | 0.00000 | 2.000000 | 3.000000 | 3.000000 | 7.000000 | 12.000000 | 13.000000 | 18.0000000 | 25.0000000 | 36.0000000 | 34 | 13.895623 | 22 |
| 1001 | 2007 | 0 | 0.0486993 | 0.0021129 | 418.57705 | 1 | 1 | 52405 | 1.443396 | 5.051887 | 9.382075 | 7.216981 | 10.825471 | 12.268868 | 7.938679 | 10.825471 | 10.825471 | 15.155660 | 8.660377 | 13.712264 | 12.268868 | 6.495283 | 3.608491 | 4.330189 | 3.608491 | 2.886792 | 0.000000 | 0.0000000 | 0.0000000 | 6.495283 | 10.825471 | 12.990566 | 14.43396 | 9.382075 | 12.990566 | 17.32075 | 14.433963 | 12.268868 | 10.825471 | 9.382075 | 7.938679 | 4.330189 | 0.7216981 | 4.3301888 | 0.7216981 | 0 | 9.250361 | 22 |
| 1001 | 2003 | 0 | 0.0116914 | 0.0002657 | 51.08138 | 1 | 1 | 46800 | 1.443396 | 2.886792 | 5.773585 | 6.495283 | 6.495283 | 11.547170 | 9.382075 | 7.938679 | 7.938679 | 12.990566 | 15.877358 | 7.216981 | 12.990566 | 13.712264 | 8.660377 | 12.268868 | 1.443396 | 2.165094 | 0.000000 | 0.7216981 | 1.4433962 | 11.547170 | 12.268868 | 12.990566 | 10.10377 | 14.433963 | 9.382075 | 12.99057 | 12.268868 | 13.712264 | 11.547170 | 16.599056 | 7.938679 | 1.443396 | 0.7216981 | 0.0000000 | 0.0000000 | 0 | 15.556297 | 22 |
| 1001 | 1999 | 0 | 0.0000000 | 0.0000000 | 0.00000 | 1 | 1 | 42963 | 1.443396 | 6.495283 | 10.825471 | 7.216981 | 13.712264 | 6.495283 | 9.382075 | 10.825471 | 10.825471 | 11.547170 | 12.268868 | 10.825471 | 10.103774 | 10.103774 | 6.495283 | 2.886792 | 4.330189 | 1.443396 | 0.000000 | 0.7216981 | 0.7216981 | 2.886792 | 9.382075 | 6.495283 | 13.71226 | 14.433963 | 20.207548 | 18.04245 | 15.155660 | 14.433963 | 8.660377 | 6.495283 | 6.495283 | 10.825471 | 2.1650944 | 0.7216981 | 0.0000000 | 0 | 14.453439 | 22 |
| 1001 | 2001 | 0 | 0.0000000 | 0.0000000 | 0.00000 | 1 | 1 | 44889 | 0.000000 | 1.443396 | 9.382075 | 4.330189 | 10.103774 | 7.216981 | 9.382075 | 8.660377 | 15.877358 | 10.825471 | 12.990566 | 10.825471 | 8.660377 | 11.547170 | 10.825471 | 6.495283 | 4.330189 | 2.886792 | 0.000000 | 0.0000000 | 2.1650944 | 5.051887 | 6.495283 | 12.990566 | 10.82547 | 17.320755 | 10.103774 | 18.76415 | 25.259436 | 7.938679 | 9.382075 | 10.825471 | 5.773585 | 4.330189 | 1.4433962 | 0.0000000 | 0.0000000 | 0 | 16.358891 | 22 |
| 1001 | 2002 | 0 | 0.0071786 | 0.0008621 | 51.13093 | 1 | 1 | 45909 | 2.165094 | 6.495283 | 7.938679 | 10.825471 | 8.660377 | 10.103774 | 10.825471 | 11.547170 | 9.382075 | 8.660377 | 5.773585 | 7.938679 | 5.051887 | 8.660377 | 14.433963 | 5.773585 | 3.608491 | 5.051887 | 1.443396 | 0.0000000 | 2.1650944 | 7.216981 | 9.382075 | 14.433963 | 14.43396 | 18.042452 | 13.712264 | 14.43396 | 3.608491 | 7.938679 | 10.103774 | 6.495283 | 10.103774 | 6.495283 | 4.3301888 | 3.6084907 | 1.4433962 | 0 | 15.043114 | 22 |

## Question 1: What is the frequency of this data frame?

Answer:

## Question 2: What is the cross-sectional (geographical) unit of this data frame?

Answer:

Step 6. Use the **names** function to display all the variables (column)
in the dataframe.

``` r
names(df)
```

     [1] "fips"           "year"           "smm"            "nox_emit"      
     [5] "so2_emit"       "co2_emit"       "nbp"            "state"         
     [9] "pop_all"        "dptp_xtile_1"   "dptp_xtile_2"   "dptp_xtile_4"  
    [13] "dptp_xtile_5"   "dptp_xtile_6"   "dptp_xtile_7"   "dptp_xtile_8"  
    [17] "dptp_xtile_9"   "dptp_xtile_10"  "dptp_xtile_11"  "dptp_xtile_12" 
    [21] "dptp_xtile_13"  "dptp_xtile_14"  "dptp_xtile_15"  "dptp_xtile_16" 
    [25] "dptp_xtile_17"  "dptp_xtile_18"  "dptp_xtile_19"  "dptp_xtile_20" 
    [29] "tmean_xtile_1"  "tmean_xtile_2"  "tmean_xtile_4"  "tmean_xtile_5" 
    [33] "tmean_xtile_6"  "tmean_xtile_7"  "tmean_xtile_8"  "tmean_xtile_9" 
    [37] "tmean_xtile_10" "tmean_xtile_11" "tmean_xtile_12" "tmean_xtile_13"
    [41] "tmean_xtile_14" "tmean_xtile_15" "tmean_xtile_16" "tmean_xtile_17"
    [45] "tmean_xtile_18" "tmean_xtile_19" "tmean_xtile_20" "mean_prcp"     
    [49] "n"             

## Question 3: Which column represents the treatment variable of interest?

Answer:

## Question 4: Which column represents the outcome variable of interest?

Answer:

Step 7: Create a boxplot to visualize the distribution of the outcome
variable under treatment and no treatment.

``` r
ggplot(df, aes(x=nox_emit)) +
  geom_histogram() +
  facet_wrap(~nbp)
```

Step 8: Fit a regression model $y=\beta_0 + \beta_1 x + \epsilon$ where
$y$ is the outcome variable and $x$ is the treatment variable. Use the
**summary** function to display the results.

``` r
model1<-lm(nox_emit ~ nbp, data=df)

summary(model1)
```


    Call:
    lm(formula = nox_emit ~ nbp, data = df)

    Residuals:
       Min     1Q Median     3Q    Max 
    -0.855 -0.855 -0.488 -0.488 67.688 

    Coefficients:
                Estimate Std. Error t value Pr(>|t|)    
    (Intercept)  0.48844    0.01555   31.41   <2e-16 ***
    nbp          0.36608    0.02276   16.09   <2e-16 ***
    ---
    Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

    Residual standard error: 2.683 on 55856 degrees of freedom
    Multiple R-squared:  0.004611,  Adjusted R-squared:  0.004593 
    F-statistic: 258.7 on 1 and 55856 DF,  p-value: < 2.2e-16

## Question 5: What is the predicted value of the outcome variable when treatment=0?

Answer: 0.488

## Question 6: What is predicted value of the outcome variable when treatment=1?

Answer: 0.488 + 0.366

## Question 7: What is the equation that describes the linear regression above? Please include an explanation of the variables and subscripts.

Answer:

$$
NOx = \beta_0 + \beta_1 NBP + \epsilon
$$

## Question 8: What fixed effects can be included in the regression? What does each fixed effects control for? Please include a new equation that incorporates the fixed effects.

Answer:

Month

Year

County

## Question 9: What is the impact of the treatment effect once fixed effects are included?

Answer:

``` r
##library("lfe")

#model2<-lm(nox_emit ~ nbp + as.factor(smm) + as.factor(fips), data=df)

#model2<-felm(nox_emit ~ nbp | fips + year, data=df)
```

# Questions for Week 5

## Question 10: In a difference-in-differences (DiD) model, what is the treatment GROUP?

Answer:

## Question 11: In a DiD model, what are the control groups?

Answer:

## Question 12: What is the DiD regression equation that will answer your research question?

## Question 13: Run your DiD regressions below. What are the results of the DiD regression?

## Question 14: What are the next steps of your research?

Step 9: Change the document format to gfm

Step 10: Save this document as README.qmd

Step 11: Render the document. README.md file should be created after
this process.

Step 12: Push the document back to GitHub and observe your beautiful
document in your repository!

Step 13: If your team has a complete dataframe that includes both the
treated and outcome variable, you are done with the assignment. If not,
make a research plan in Notion to collect data on the outcome and
treatment variable and combine it into one dataframe.
