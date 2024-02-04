# Description
This repository is one of the products of the thesis called "Designing a semi-automated approach to find potential evidence of corporate greenwashing" that I conducted in partial fulfillment of the requirements for the degree of Master of Science in Engineering and Policy Analysis at Delft University of Technology. This thesis was publicly defended on January 16, 2024. This thesis can be found on the official TU Delft repository [here](https://repository.tudelft.nl/islandora/object/uuid%3Aca6976fe-c1a0-4aa2-89b2-662ba4212e6e?collection=education). The abstract follows below.

This repository contains the data that my thesis was based on and produced. Moreover, codes and files that were used to elaborate the original data and produce results are also shared. The thesis report is also shared in this repository along with the a PowerPoint presentation about it that was used to defend this thesis.

## Thesis abstract
Greenwashing can be defined as the mismatch between companies’ positive green communications and their activities that are counterproductive to the fight against climate change. Greenwashing companies can undermine the success of climate policies by hiding their climate footprints and prevent policymakers from realizing the need for further regulations. Thus, the identification of greenwashing should be done timely: this research sets out to find a semi-automated approach that can find evidence of greenwashing. The study of greenwashing is limited to the mismatch between companies’ communications on official websites and their lobbying activities in the European Union. Some steps of the design research approach were used namely the design development, demonstration, and evaluation (via a small-case evaluation) phases. The created approach measures companies’ communication levels of commitment to climate change using a GPT-based sentence classifier and then compares it to their levels of lobbying on climate change using keyword-based filtering on the EU Transparency Register, the official lobbying source for the EU. The proposed method is semi-automated at this stage and can inform a greenwashing appraisal, but it has issues with the accuracy of its analysis. This research partially fills the gaps in the greenwashing literature and advances the research in the use of GPT for classification purposes and in the field of climate lobbying in the EU. This research can teach the implementation of new EU regulations that aim at banning greenwashing: the more detailed the definitions of greenwashing that are used, the easier to find greenwashing automatically, and, therefore, the faster the enforcement of the ban can be. 

# How to use
The repository is divided in two parts:
* Approach: this part contains the sources that describe the approach created. This folder is further divided in three: "1 - Communication" and "2 - Lobbying" which describe the two respective parts of the approach and "3 - Greenwashing table" which describes how to present the final results to allow for a greenwashing appraisal.
* Demonstration: this folder contains the demonstration results of the use of the created approach on two companies, ExxonMobil and Shell. The original data and the results of the analyses are present in this folder. The folder is further divided in "1 - Communication" and "2 - Lobbying" which describe the applications of the two respective parts of the approach and "3 - Greenwashing table" which contains the table that presents all the results of the two previous parts in a way that allows for a greenwashing appraisal.

There are further README.md that describes the particular sections of this repository.

# Folder structure
``` bash
.
├── Approach/ # the sources behind the approach 
|   ├── 1 - Communication/ # the communication part of the approach
|       └── README.md # README that describes this folder
|   └── 2 - Lobbying/ # the lobbying part of the approach
|       └── README.md # README that describes this folder
|   └── 3 - Greenwashing table/ # a mockup of the display of the final results
|       └── README.md # README that describes this folder
|
├── Demonstration/ # the data and results of the approach demonstration
|   ├── 1 - Communication/ # the demonstration of the communication part of the approach
|       └── README.md # README that describes this folder
|   └── 2 - Lobbying/ # the demonstration of the lobbying part of the approach
|       └── README.md # README that describes this folder
|   └── 3 - Greenwashing table/ # the displaying of the final results of the demonstration
|       └── README.md # README that describes this folder
|
├── Thesis report.pdf # the report of the thesis.
└── Thesis presentation.pptx # the PowerPoint presentation of this thesis.
```