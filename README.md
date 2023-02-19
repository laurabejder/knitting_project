# Knitted Knockers
This project dives into the world of knitted breast prostheses on the knitting platform [Ravelry.com](https://www.ravelry.com/). It explores how breast cancer survivors knit new breasts for themselves (and others) after they have undergone mastectomy surgeries. 
The result is the article [Medical Knitting: How Breast Cancer Survivors Handle Mastectomies One Knitted Knocker at a Time](https://laurabejder.com/knitting/).

## In this repository
### Notebooks
- `data_collection.ipynb`: This notebook scrapes the knitting recipes in the 'medical knitting' subcategory on Ravelry.com and gathers information on the pattern and their popularity among the ravelry community. 
- `data_analysis.ipynb`: This notebook analyses the data gathered in `data_collection` alongside data from the CDC and manually collected data on the recommended yarn for the knitted knockers (the often used name for knitted breast prostheses) and the price of the yarn.
- `data_visualization.ipynb`: This notebook uses the R package ggplot to create the basic visualization of the data. The visualizations were later imported to Adobe Illustrator and then converted into responsive html using [ai2html](http://ai2html.org/). 

### Inside the `data` directory
Inside this directory, you can find all the data used in the analysis.

### Inside the `visuals` directory
This directory contains the outputs of the ggplots created in `data_visualization.ipynb` and the versions edited in Adobe Illustrator.

## Project description

### Aim of the project
The aim of this project is to examine the use and popularity of the knitted knockers recipes among the ravelry.com users. It looks in to the popularity of the recipes compared to other categories of recipes in the "medical knitting" subcategory, examines the price of a knocker by looking at the recommended yarn and puts the concept into the larger context of high breast cancer rates among women compared to other types of cancer. 

### Findings
I found that knitted knockers are the by far most popular category of recipe in the medical knitting subcategory. This is measured by the number of completed projects registred on Ravelry.com. 

I also found that knitted knockers are a cheaper alternative to conventional breast prosteses.

### Data collection

- The data in `patterns_total.csv` was gathered by scraping the [medical knitting](https://www.ravelry.com/patterns/search#pc=medical&sort=popularity&view=captioned_thumbs) category of Ravelry.com
- All the data on the price of the yarn for the knockers presented in `knockers_yarn_details.csv` was manually gathered from the recipes and the websites of the retailers of the yarn. 
- I also manually collected a sample of prices of conventional breast prostheses using Google. The data can be found in `prosthesis_info.csv`. It wasn't used in the article as I decided to go with the price ranges on [breastcancer.org](https://www.breastcancer.org/treatment/surgery/breast-forms/types) as a measure for the price of conventional prostheses instead. 
- The data on cancer rates comes from the [CDC's cancer statistics](https://gis.cdc.gov/Cancer/USCS/#/AtAGlance/).

### Data analysis process
After having collected information on all the recipes in the medical knitting category, I manually categorized all of the recipes. In some categories there were a lot of recipes while other categories only has one or a few recipes. 7 of the recipes did not have a medical purpose, so they were categorized as `na`. Knitted knockers are the second largest category after heating/cooling bags. 

|Category|n of recipes|
|------|-------|
|heating_cooling	|41|
|knockers	|29|
|cannula_iv	|20|
|injury	|19|
|menstruation	|14|
|maternity	|13|
|cast_cover	|12|
|na	|7|
|pain_relief	|5|
|amputee	|3|
|respiratory	|2|
|fertility	|2|
|stoma	|2|
|mental_psycological	|1|

Afterwards I used pandas to group the number of projects by recipe category. 

### New skills
For this project I used Adobe Illustrator and ai2html for the first time. Although the outcome is not perfect, I think it turned out ok considering it is a first attempt. I learned a lot about how to create a chart in ggplot, export it to a pdf, tweak in in Illustrator and embed it in html using ai2html including creating several versions of each chart and including the necessary JavaScript element in the html.  
