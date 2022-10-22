Project Proposal by Yue Ma
================
Yue Ma

# Introduction to problem/question

Compare the performance of different time series classification models

# Problem / Question

Time series data is of tremendous importance in the field of
environmental sustainability. Exploring this kind of data helps us
understand the pattern of ecosystems, which allows us to detect the
abnormal changes in time and help the relative department to make
decisions. In this study, I will compare the performances of two
state-of-the-art time series classification (TSC) models, fully
convectional neural network (FCN) and deep Residual Network (ResNet).

# Inspiring Examples

## Example 1

![](http://www.timeseriesclassification.com/images/datasets/Crop.jpg)

As shown in the figure, different types of objects have different time
series data features, and this kind of pattern can help us to
distinguish them. Besides, by analyzing time series data, we can detect
the abnormal change within one class and make according response to it.

## Example 2

![](https://ieeexplore.ieee.org/mediastore_new/IEEE/content/media/7958416/7965814/7966039/7966039-fig-1-source-large.gif)

The structure of these two deep learning models are shown in the above
figures.

## Example 3

![](https://ieeexplore.ieee.org/mediastore_new/IEEE/content/media/7958416/7965814/7966039/7966039-table-1-source-large.gif)

The results shows that the models have comparable performance on
univariate datasets, but how will they perform on multivariate datasets?

# Proposed data sources

[land cover classification
dataset](https://wapor.apps.fao.org/catalog/WaPOR_2/1/L1_LCC_A): In this
study I assume that the land cover type does not change within one year.

[NDVI data](https://lpdaac.usgs.gov/products/mod13q1v006/): The time
period of the NDVI data is from 2009 to 2016.

[CHELSA dataset](https://chelsa-climate.org/downloads/): monthly
precipitation data, temperature data (mean) from 2009 to 2016.

[soil
data](https://github.com/AdamWilsonLab/emma_envdata/releases/download/processed_static/soil_Total_N_.tif):
In this study I assume that the soil type data of the study area does
not change from 2009 to 2016.

[topodiversity
data](https://github.com/AdamWilsonLab/emma_envdata/releases/download/processed_static/alos_topodiversity.tif):
topographic diversity stands for the variation of landforms present in
an area. In this study I also assume that the topographic diversity of
this study area does not change during this time period.

The data used in this study is in two categories: static and dynamic.
The precipitation data and temperature data are considered as dynamic
data while the soil data and topodiversity data are considered as static
data. (Another potential research question for this study is whether the
static and dynamic data have same importance in this classification
task)

# Proposed methods

This study can be divided into four parts:

1.  data collection and pre-processing: In this part, I collected the
    aforementioned data and normalized them into the same value range
    (Except the NDVI data). The normalized value range for the NDVI data
    is \[-1,1\], while the normalized value range for the other
    envrionmental variables is (0,1\].

2.  build training and testing datasets: Based the land cover
    classification data, I select pixels that do not change during the
    study period and build a mask based on them. This mask is then
    applied to select pixels from the NDVI and environmental variables
    data. Then the label from the classification data and the data from
    previous step are combined together and then splited into training
    and testing datasets.

3.  build and train deep learning models: The deep learning

4.  discussion:

# Expected results

After the training part, I will get two well-trained models. Then I will
use the test dataset to evaluate their performance and get the results.
The comparison result will be displayed in a table.
