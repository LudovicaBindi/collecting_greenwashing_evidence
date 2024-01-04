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

# Analysis explanation
The goal of this analysis is to quantify the lobbying data in order to compare it with the communication analysis results.

The data comes from the Transaprency Register:
* the data can be downloaded from the company's page on the web version of the Transparency Register (https://ec.europa.eu/transparencyregister/public/consultation/search.do?locale=en&reset=) or can be downloaded in an easier-to-user Excel format from the company's page on LobbyFacts (https://www.lobbyfacts.eu/)

To analyze the meetings of companies with Commissioners, Cabinet Members, and Director-General and get the number of meetings that are relevant to climate change regulations, I ran a keywords-based filtering. The filtering is on the “Subject” field of the data downloaded from LobbyFacts (on the PDF downloadable from the TR the field is called “Subject(s)”). A keyword analysis was deemed enough to make an informed filtering decision because of the simplicity of the text that describes such meetings: these are just small sentences without verbs that tell the key topics discussed during the meetings.

The main part of this process is the keywords that I use for the filtering. The keywords that I ended up using can be divided into two main categories:
* Specific legislation. Following Kim et al. (2016), I picked the most prominent climate regulations that have been discussed throughout the years. Examples of these policies are the “European Green Deal”, “Paris Agreement”, and the “ReFuelEU Aviation Regulation”. Some of the less recent regulations (such as the Green Deal) were included because these lists include meetings since the end of 2014. To get the names of such legislation I searched on Google for “key eu climate legislation” and stopped my search when I didn’t find any new results. Moreover, I also used my own knowledge of important legislation to form such a list.
* General climate change words. These words represent the main keywords and buzzwords around climate change. Examples of these are “climate change”, “renewable energy”, and “decarbonization”. Moreover, from the keywords I got from these sources, I removed those words that are more likely to create false positives in the filtering because such words could be used in different contexts that are not related to climate change. These words were “carbon” because it could be discussed as an element on its own for some products, and “climate” and “environment” because they could be used to describe the mood of something (e.g., “political climate”).

These keywords want to capture all the meetings that are more likely to be lobbying on specific regulations or that discuss climate change in general. I included in the keywords also related words, synonyms, and acronyms of the original list for more accurate filtering. Different spellings and all the plurals of the words were included for an easier filtering process.

To conduct the filtering, I used Python and the library “re - Regular expression operations” to find the exact matches of keywords. I didn’t consider the capitalization of words as relevant (therefore, I first transformed all descriptions and keywords into lowercase) because I assumed that mistakes in capitalization could easily happen. For the actual filtering, a meeting was deemed relevant to climate change if any of the keywords were found in the description. Finally, the share of the relevant meeting was computed as the number of relevant meetings over the total meetings recorded.
