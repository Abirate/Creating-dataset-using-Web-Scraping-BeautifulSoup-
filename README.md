# Creating-dataset-using-Web-Scraping-BeautifulSoup-
English quotes dataset for NLP tasks 

## Dataset Summary
english_quotes is a dataset of all the quotes retrieved from [goodreads quotes](https://www.goodreads.com/quotes). This dataset can be used for multi-label text classification and text generation. The content of each quote is in English and concerns the domain of datasets for NLP and beyond.

## Supported Tasks
- Multi-label text classification : The dataset can be used to train a model for text-classification, which consists of classifying quotes by author as well as by topic (using tags). Success on this task is typically measured by achieving a high or low accuracy.
- Text-generation : The dataset can be used to train a model to generate quotes by fine-tuning an existing pretrained model on the corpus composed of all quotes (or quotes by author).

## Languages
The texts in the dataset are in English (en).

## Dataset Structure
#### Data Instances 
A JSON-formatted example of a typical instance in the dataset:
```python
{'author': 'Ralph Waldo Emerson',
 'quote': '“To be yourself in a world that is constantly trying to make you something else is the greatest accomplishment.”',
 'tags': ['accomplishment', 'be-yourself', 'conformity', 'individuality']}
  ```
 #### Data Fields
 - **author** : The author of the quote.
 - **quote** : The text of the quote.
 - **tags**:  The tags could be characterized as topics around the quote.
 
  #### Data Splits
I kept the dataset as one block (train), so it can be shuffled and split by users later.

## Dataset Creation
#### Curation Rationale
I want to share my datasets (created by web scraping and additional cleaning treatments) with the AI community so that they can use them in NLP tasks to advance artificial intelligence.

#### Source Data
The source of Data is [goodreads](https://www.goodreads.com/?ref=nav_home) site: from [goodreads quotes](https://www.goodreads.com/quotes)

#### Initial Data Collection and Normalization 

The data collection process is web scraping using BeautifulSoup and Requests libraries.
The data is slightly modified after the web scraping: removing all quotes with "None" tags, and the tag "attributed-no-source" is removed from all tags, because it has not added value to the topic of the quote.

#### Who are the source Data producers ? 
The data is machine-generated (using web scraping) and subjected to human additional treatment. 

In the repositry, I provide the script I created to scrape the data (as well as my additional treatment):

#### Annotations 
Annotations are part of the initial data collection (see the script).

## Additional Informations
#### Dataset Curators
Abir ELTAIEF :
[@AbirEltaief](https://tn.linkedin.com/in/abir-eltaief-pmp%C2%AE-469048115)


#### Licensing Information 
This work is licensed under a Creative Commons Attribution 4.0 International License (all software and libraries used for web scraping are made available under this Creative Commons Attribution license).

#### Contributions 
Thanks to [@Abirate](https://github.com/Abirate)
 for adding this dataset. 
