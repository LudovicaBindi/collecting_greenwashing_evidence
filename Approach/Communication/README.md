# Description

During the process I tried different structures of the sub-tree, creating different middle labels. Therefore, some of the labels name that you will see in the files (including the files name) are not present in the final tree because these labels didn't yield the best accuracy and, therefore, were dropped.

# How to use
There are two files that faciliate the reusability of this research:
* "all sentences - labeled.xlsx" contains all the data that was used to inductively create the codes. This data is fully labeled. Therefore, this data can be easily reused by other researchers.
* "Communication part of the approach - Description and prompts.xlsx" contains the prompts that are the key to the classification via GPT. There are instructions to follow and there are already sheets that can be easily used (by filling them with the data that researchers produce following the instructions) to facilitate the running of this analysis on new data.

In the "prompts creation process" folder, I put the different tests that were conducted to create the tree and matching tree structure that is to be used to classify the sentences. The resulting tree structure can be see in the following picture. The files names have these rules:
* the basic version of the name is "[root label]_[child label 1] vs [child label 2] vs [child label ...] _ res.xlsx" where "root label" is the label the categorization is carried out within and whose "child labels" are being categorized. 
* If there is a "VX" it means that this is a new version of the original categorization: a new version means that the subtree structure has been modified.
  * Each file is in the folder called as the level where the labels that are being classified belongs to. For example, the file that discusses the classification between "company_beliefs" and "common_beliefs" (which happen within the "stance_on_CC" label) is in the "Level 3" folder because these two labels are at third level of the tree as seen in the picture below (for reference, the name of this file is "stance_on_CC_V2_company_beliefs vs common_beliefs_res").

All the files present a sheet called "README" that briefly describes them. It is advised to read the different versions of the same categorizations to understand the tree and prompts creation process.

Some of the files name present some abbreviation:
* decl. = declaration
* priorit. = priorities
* gen. = general
* detail. = detailed


 

<p align="center">
  <img src="S3C2 - NEW labels tree-tree for classification - FINAL CLASSIFICATION STRUCTURE.drawio.png" width="1000" title="hover text">
</p>


# Folder structure
``` bash
├── prompts creation process/ # contains the prompts creation process
├── all sentences - labeled.xlsx # data used for the inductive creation of the codes
└── Communication part of the approach - Description and prompts.xlsx # Analysis instructions and prompts

```

``` bash
.
├── Approach/ # the sources behind the approach 
|   ├── Communication/ # the communication part of the approach
|       └── README.md # README that describes this folder
|   └── Lobbying/ # the lobbying part of the approach
|       └── README.md # README that describes this folder
|
├── Demonstration/ # the data and results of the approach demonstration
|  ├── Communication/ # the demonstration of the communication part of the approach
|       └── README.md # README that describes this folder
|   └── Lobbying/ # the demonstration of the lobbying part of the approach
|       └── README.md # README that describes this folder
└── Thesis report.pdf # the report of the thesis.
```