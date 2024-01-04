# Description
This folder contains how to display the final results of the communication and lobbying analyses in a way that allows for a greenwashing appraisal. This is the final part of the approach.

# How to use
The file "Greenwashing table - mockup.xlsx" contains a table with the results of the analyses on some companies. This company can be used directly by simplying changing the data inside (that is, keep the settings of the color coding of the cells the same). Follow the instructions on the file.

# Folder structure
``` bash
.
└── Greenwashing table - mockup.xlsx # the mockup greenwashing table which can be direclty re-used
```

# Analysis explanation
In this step of the approach the data that has been produced from the previous steps is collected and displayed:
* regarding the communication, the percentage of the "relevant" sentences that fall within the "stating_intentions", "acknowlege_importance", "support_for_policy", "support_for_government", "company_beliefs", and "common_beliefs" are displayed.
* for the lobbying, the percentage of relevant meetings to climate change (that is, the result of the filtering process) is displayed along with the average total expenditures of the company that is decleared on the Transparency Register
    * the total expenditure number is provided as value brackets (e.g., 400 000 – 499 999) and, therefore, on this final table I only display the average of the upper and lower brackets.
    * the data of the total expenditures can be seen on the company's entry on the Excel version of the Transparency Regsiter (downloadable from https://data.europa.eu/data/datasets/transparency-register?)locale=en or consulted it on the company's entry on the web version of the Transperncy Regsiter (https://ec.europa.eu/transparencyregister/public/consultation/search.do?locale=en&reset=)

The table created here presents all the communication and lobbying data displayed with each cell color-coded according to their position on the values scale of their corresponding variable (darker color represents higher values). The color coding is possible for all the variables (note that each variable has its own color-coding rule): for the communication, I use the percentage of sentences that fall within the final labels which has an inherent scale of 0 to 100 and the same applies for the percentage of relevant meetings for the lobbying analysis; finally, the total expenditures variable’s scale comes from the Transparency Register itself: companies do not declare absolute values but brackets within which their expenditures fall, and in Transparency Register the lowest bracket they can declare is “< 10 000” and the highest is ” ≥ 10 000 000”. Therefore, I used 0 as the lower bound and 10,000,000 as the upper bound. To create the color coding, I used Excel conditional formatting where the colors with the highest (lowest) possible number on the scale are matched with the darkest (lightest) color, and all the numbers in between are spread uniformly on the scale.