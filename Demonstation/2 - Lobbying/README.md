# Description
This folder contains the data of the demonstration of the lobbying part of the approach. The demonstration has been carried out on ExxonMobil and Shell.

# How to use
The folder "Original data" contains the data that was analyzed:
* The "Companies entry from TR.xlsx" contains the data that was present on the TR of the companies (including the total expenditures)
* The "ExxonMobil_meetings.csv" and "Shell_meetings.csv" are the lists of meetings of the two companies directly donwloaded from LobbyFacts.

The folder "Processed data" contains the results of the analysis:
* The "Total expenditures.xlsx" contains the average of the total expenditures of the companies as described on the "Approach/2 - Lobbying/README.md" file.
* The "ExxonMobil_meetings_filtered_with counts.xlsx" and "Shell_meetings_filtered_with counts.xlsx" are the results of the filtering process whose code is in the "Approach/2 - Lobbying/Running lobbying analysis of companies' meetings.ipynb" file. The total number and percentage of relevant meetings are displayed in these files.

# Folder structure
``` bash
.
├── Original data/ # the input data for the analysis: TR entries and meetings lists
|
└── Processed data/ # the results of the analysis: total expenditures average and meetings lists analyzed
 
```