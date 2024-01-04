# Description
This folder contains the different trials and results of creating the final tree structure of the labels that you see depicted below ant that is the one used in the communication part of the created approach.

During the process I tried different structures of the sub-tree, creating different middle labels. Therefore, some of the labels name that you will see in the files (including the files name) are not present in the final tree because these labels didn't yield the best accuracy and, therefore, were dropped.

# How to use
There are two files that faciliate the reusability of this research:
* "all sentences - labeled.xlsx" contains all the data that was used to inductively create the codes. This data is fully labeled. Therefore, this data can be easily reused by other researchers. Moreover, this file contains a description of all the labels (both original and final trees).
* "Communication part of the approach - Description and prompts.xlsx" contains the communication part of the created approach. It contains the prompts that are the key to the classification via GPT. There are instructions to follow and there are already sheets that can be easily used (by filling them with the data that researchers produce following the instructions) to facilitate the running of this analysis on new data. This is the resulting approach from the whole creation process whose (intermediate) results are present in the "prompts creation process" folder.

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

Each of these files has the same sheets:
* <i>README</i>: contains a brief description of what is being tested in the file.
* <i>training sentences</i>: the sentences and their labels being used in the file.
* <i>results</i>: the results of the different classifications using the different prompts (listed in the "prompts" sheet). Note for each prompt I ran the classification twice (that is, I used GPT twice to classify the sentences. That's why in the file there are two "rounds" of classification results)
* <i>prompts</i>: the descriptions of the prompts used for the classification.
* <i>testing</i>: used for some testing where I manually change the results of the GPT classification to see how the accuracy would change if GPT had given a different answer to the classification. There is a description of what I am testing on at the beginning of the file. This sheet is not always present.


<i>Figure 1. The created tree structure that is used to classify the sentences.</i>
</br>
<p align="center">
  <img src="pictures/S3C2 - NEW labels tree-tree for classification - FINAL CLASSIFICATION STRUCTURE.drawio.png" width="1000" title="final tree">
</p>

# Folder structure
``` bash
├── prompts creation process/ # contains the prompts creation process
|   ├── Level 1/ # all the files that describe the classifications happening at level 1
|   ├── Level 2/ # all the files that describe the classifications happening at level 2
|   ├── Level 3/ # all the files that describe the classifications happening at level 3
|   └── Level 4/ # all the files that describe the classifications happening at level 4
|
├── pictures/ # contains the pictures depected in this README
|
├── all sentences - labeled.xlsx # data used for the inductive creation of the codes
└── Communication part of the approach - Description and prompts.xlsx # Analysis instructions and prompts

```


# Data collection and data processing 
There are two steps of the analysis in this folder collected: in the first, I inductively coded some sample sentences that I collected; in the second, a created a tree that enable to properly code these sentences in a deductive manner via GPT. What follows is a summary what is discussed more thoroughly in the thesis report stored at the root of this repository.

### Step 1: Inductive coding
The sample companies that were chosen were: Saudi Aramco, Amazon, Sinopec Group, Volkswagen, Uniper, and McKesson.

After selecting the companies, I gathered these companies’ online communications data. For each company, I searched on Google for “climate” and restricted the results to companies’ official corporate websites by adding “site:company-website.com” to the query (see Appendix A – Figure 5 for these websites). Moreover, I selected those articles that seemed to potentially contain the stance of the company on the topic. I stopped selecting articles once I saw that further Google results were less significant and/or when I saw that I had analyzed a similar number of sentences compared to the rest of the companies. To enrich my dataset with more stances that could give a greater variety of opinions, I repeated this research and analysis with a different keyword. For each company, I picked a climate change-related topic that the sector of the company is associated with. I chose these topics assuming that the companies would present multiple results on such ad-hoc topics. Table 1 contains the topics selected for each company.


<i>Table 1. The ad-hoc topics for each company based on their sectors.</i>
| Company   | Sector | Topic |
| -------- | ------- | ------- 
| Saudi Aramco, Sinopec Group | oil | il spill |
| Amazon | internet service and online retail | waste |
| Volkswagen | car manufacturing | greenhouse gas emssions |
| Uniper | energy | greenhouse gas emssions |
| McKesson | health | energy efficiency |

The goal of the analysis was to better understand what companies were saying around the issue of
climate change and what were the similarities between companies via a qualitative data coding process. Having gathered all the sentences of analysis, the first round of analysis was deductive coding:  I first separated them between “relevant” and “not relevant”. “Relevant” sentences contained a “clear” claim from the company. That is, there should be a topic on which the company
says something, and what they say is their position (so they are making a statement regarding
themselves). Thus, these sentences contain the company’s stance on the issue. The topic is mainly
related to climate change because that's what I was searching for in the Google query, but I also got a
couple of sentences that showed some kind of opinion on some other topic (e.g., workers' safety). The
“not relevant” sentences were all the rest of the sentences. After having read the articles I picked, I
re-read all the sentences I collected and re-checked all the labels. This process was iterative: for
example, understanding the categories was iterative in the sense that I first started with classification,
and by reading more and more sentences I changed the details of my initial classifications because I
better understood how the companies were communicating. And therefore, I had to re-read the
sentences. In this first round of analysis, I also saw that companies made general statements regarding a climate change topic which express some general stance or call to action. Since there was quite a relevant number of such kinds of sentences, I decided to make a new category for them, “relevant_general” (thus, this category was achieved via inductive coding). While these sentences do not necessarily imply a company pledging environmentalism, it was decided to keep these sentences in the analysis because of their numbers and because they show at least some kind of awareness from the companies regarding the issue.

In the second round of coding, I analyzed the sentences in the two categories that were deemed relevant (“relevant” and “relevant_general”) in an inductive manner. How I approached the analysis: I created the sentences in a hierarchical approach by first creating more general labels and then specializing them in the following rounds of analysis. I used the following rules to decide when to stop with label creations:
* I wanted to avoid overfitting the labels to the data I gathered for the specific companies I analyzed. Thus, labels that are too specific to the data could become irrelevant when applying the method in the evaluation of the whole pipeline. For example, I am not making the category "declaration_of_net_zero_target" vs "declaration_of_scope_1_reduction" but instead keeping a more general "declaration_of_target"
* I stopped when the sub-class sizes were becoming so small that adding another subclass would lead to such small groups (e.g., just a couple of sentences). This, in turn, would also lead to overfitting.
* Due to time limitations, I limited the tree of hierarchical categories to a depth of four.

Note that I analyzed the “relevant” and “relevant_general” sentences separately and, in this way, created two branches of inductive coding trees.

The resulting tree of these codes can be seen in Figure 2.

<i>Figure 2. The original tree structure</i>
<p align="center">
  <img src="pictures/S3C2 - Labels tree-Labels ordered of intensity.drawio.png" width="1000" title="final tree">
</p>


### Step 2: Creation of GPT-based deductive coding tree
To better make sense of the final labels that I created, I re-arranged them according to the focus that
these sentences: some discussed actions that the company takes or has intentions to take, some
discussed the stance that the companies have on specific policies or government’s actions, and the
others contained the stance that companies have on climate change in general. The re-ordered
tree is in Figure 3. 

<i>Figure 3. The re-ordered tree (not the final tree, yet).</i>
<p align="center">
  <img src="pictures/S3C2 - NEW labels tree.drawio.png" width="1000" title="final tree">
</p>

In this approach, GPT is used to deductively code the previously identified codes to the sentences that can be found in the online communication of a company. The method entails creating a prompt that directs GPT into coding the given sentences as one of the codes presented in the prompt.
For creating the model, I took into consideration how to write prompts to effectively use LLMs and to optimize for the accuracy of the classification tasks. Moreover, I leveraged the labeled data that I had to both create more accurate prompts via few-shot learning and to test the accuracy of the coding. Note that I used the ChatGPT web interface to run the model creation because it has easy-to-use interactive features.

To use ChatGPT efficiently, I used prompt engineering principles. I used few shot learning, that is I wrote prompts that described the task at hand with a few examples of the task to be executed (few-shot learning). Another technique from prompt engineering that can be used is explaining the reasoning behind the examples provided to increase the precision of the LLM. Therefore, when creating the classification method, to increase accuracy I increased the number of examples in the prompts. If that wasn’t enough, I then proceeded to give small explanations of the coding decision behind the provided examples but this happened in a few situations. To test for the accuracy of the GPT coding, for each round of coding that I did, I randomly picked 30 sentences (or, if the batch of sentences to pick from was smaller than 30, then as many sentences as possible were used as the testing sample) from the labeled data that belonged to the labeled data whose coding I was testing and that were not in the prompt I was using. I asked GPT to code these sentences and then checked the accuracy of the labels by comparing the GPT produced and the original labels. Note that this data was only used for testing purposes since this data didn’t inform the model creation: to increase accuracy I just increased the number of examples, picked better examples for the few-shot learning prompts, and/or added explanations to the examples.

Another principle that I applied when creating my method is that GPT performed better when
the number of codes that I was asking it to code where small in number compared to when I asked to
classify all the larger amounts of labels. 

With these two considerations in mind, I approached the coding of the final labels that I found
in a cascade manner: starting with the tree depicted in Figure 3, GPT first coded the upper labels (for
example, “actions”, “stance_on_policy”, and “stance_on_CC”) and then, based on these upper
classifications GPT was used to code the lower labels: that is if a sentence was coded as “actions”,
then GPT was used to code it as one of the
“actions” labels in the figure. This is done in order
to limit the number of labels that GPT has to code
in one round which can be beneficial to the
accuracy as described above. Moreover, I created
intermediate labels between the labels that are
present in Figure 1 in order to maximize the
accuracy of the coding. In this way, I created the final classification tree which was presented at the beginning of this README, in Figure 1. 

Two practical considerations that I also applied. First, to overcome the limitations of non-determinism discussed previously, for each prompt that I tested, I ran two rounds of coding with GPT and got the average of the accuracy to represent the accuracy of the prompts. Secondly, due to time limitations reasons, I decided to stop improving the accuracy of the prompts when I reached an accuracy of around 80%.