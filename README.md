# 2015 US Mortality Data: Risk Factors for Suicide

## Abstract
The value of life is priceless. However, each year, more than 40,000 people die by suicide in United States. Suicide is a major public health concern and is the 10th leading cause of death in the US. 

Luckily, suicide is preventable. Knowing risk factors for suicide can help prevent suicide. Risk factors for suicide are those characteristics associated with suicide, characteristics that make it more likely that individuals will consider, attempt, or die by suicide. They might not be direct causes.

This project explored single factor such as sex, age, marital status and the intersecting combination of them to see are those characteristics associated with suicide.

The hypothesis verified in the project includes:
- Are men more likely to suicide than women?
- Are teenagers more likely to suicide?
- Does marital status influence suicide?

Besides answering the questions above, I also found some interesting facts of the comprehensive effect of combination of single factors, such as :
- Men who are single are much more likely to suicide 
- Women who are widowed are less likely to suicide
- Young men are more likely to suicide
- Elder women are less likely to suicide.

## License and Terms
[MIT License](https://opensource.org/licenses/MIT)

[CC0: Public Domain](https://creativecommons.org/publicdomain/zero/1.0/)


## Data

### Source Data

Data used in this project is 2015 US Mortality Data downloaded from [CDC’s National Vital Statistics Systems](https://www.cdc.gov/nchs/data_access/vitalstatsonline.htm#Mortality_Multiple). It's under [CC0: Public Domain](https://creativecommons.org/publicdomain/zero/1.0/) license. The data includes 77 columns and 2,718,198 rows.

In raw data, values of each column are represented by codes. The description of codes is stored in ```2015_codes.json```.

## Data Process and Analysis

Prerequiste Packages:

- pandas

- numpy

- matplotlib.pyplot

First, I performed a overall statistics analysis of the whole dataset to see how many death records do I have, and among those how many records are caused by suicide.

I extracted suicide records out as sub dataset then I respectively classified whole dataset and suicide sub dataset by sex, marital status, and age. For each factor, I analyzed the count distribution of that factor among suicides. To have a different view of the effect of the factor, I also calculated the suicide ratio of each group. It's defined by Count of Suicide of that group / Count of Total Death of that group * 100%. Suicide ratio is a clearer indicator to show which group are more likely to suicide and which group are not.

Since causes leading a human behavior are complex, we should also consider conprehensive effect of mixed factors besides of only considering effect of single factor in human-centered data science. Thus besides analyzing the effect of single factor, I also performed analysis on intersecting combinations of thoes single factors to figure out the comprehensive effect of mixed factors. The method is as similar as that of analyzing single factor.


```Risk Factors for Suicide.ipynb``` contains all code and information of data processing and analysis.


## Directory Structure
```
data-512-final-project (master)
|
|     License
|     README.md
|     Risk Factors for Suicide.ipynb
|	    2015_data_sample.csv
|	    2015_codes.json

```

