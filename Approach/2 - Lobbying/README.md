# Description
This folder contains the part of the approach that deals with the analysis of the meetings to determine whether they are related to climate change or not via a keyword-based filtering.

# How to use
The code that runs the analysis is contained in the "Running lobbying analysis of companies' meetings.ipynb" notebook. The keywords are present in the "lobbying_climate_keywords.xlsx": each row presents a keyword in the "Original keywords" column and its synonsyms, related words, different spellings, etc. of that keyword in the "synonyms/related" column.

# Folder structure
``` bash
.
├── Input/ # contains the list of meetings to analyze 
|
├── Output/ # contains the results of the analysis
|
├── lobbying_climate_keywords.xlsx # the climate change-related words
└──  Running lobbying analysis of companies' meetings.ipynb # the notebook to use
```