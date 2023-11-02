## Context

### What

Explore relationships between personal Google location based activities and calories burnt. This is intended for those aware or interested in data science techniques, as well as interested in exploring their own activity calorie data.

##### Why

To find surprising insights that could inform healthier life choices, and to give personalised answers to questions such as: "In which season(s) do I tend to get more calories burnt in transit?" or "Do I tend to burn more calories in transit when commuting or other activities?". 

### How

![Analysis pipeline](images\analysis_pipeline.png)

(The pipeline was generated with PlantUml: [source](https://www.plantuml.com/plantuml/uml/ZLFDZjGm3BxFKrYzy2Fr5T2Y4U824aBS20UJVDE9I9tYEB0ZnBj3gTgYQ7PdZuq_-_knUrUCrUgO3XEhHOjPgFkWc5X1ANkUNqf7lmxq_EKBwZKEP-jVKVSkSzW0JiwnMDOB1JOkiEv0_Omw9h0KaDIKIlkOyaydFiif1eZ7lzuLyn6XUf1dmv0rUavEJc2hYctE9sKffwmZhPLdD7-oxLHd-6yKnJ1ej4jt-7tD9-wXFXOiFliwRGQtYfF6sPjxK_P68tH0pryJTe4DpViPieVfX2LSvLoGJKmBGt0oPzYEFkPngeOjW7tOt5-BGSdMc9ni6bQEjvhhz3_2C4vPEL4Rzb711YeOMInw9rDY3tfu9twH5foqssbCl1PEbu9D-UxAM0UO4_ASiaQKbMuJbLMHPbtVAyiyxmTslgke58rRs7RMyut_rVRWxgd_V8uXGBuy-JzOTjfsFdfWZs-kdRIVpUtSskRRPt872NLCVm00))

This depends primarily on personal data of semantic location history retrieved from Google (steps below). And this is joined with a basic calories burnt per activity dataset from Kaggle: https://www.kaggle.com/datasets/aadhavvignesh/calories-burned-during-exercise-and-activities 

Locations are mapped using a simple plot over map image: https://commons.wikimedia.org/wiki/File:BlankMap-World-Equirectangular.svg (Note: this should be upgraded to a library, as the map projection doesn't fit standard coordinates)

## Prerequisites

### Google Semantic Location History

Here are the steps to retrieve Google Sematic Location History from Google Takeout ready for analysis:

1. Go to https://takeout.google.com/settings/takeout
2. Select only "Location History" (and deselect all other options)
3. Select "JSON" as the export format
4. Click "Next step"
5. Select "Send download link via email"
6. Click "Create export"
7. Wait for the email to arrive (it may take a few hours)
8. Download the email's export zip file 
9. Extract the 'Semantic Location History' folder to this project root

### Install python and libraries

1. Install Python: 3.12.0
2. Install Pip: 23.3.1
3. Install dependent libraries: `pip install -r requirements.txt`

## Running the analysis

1. Step though `analysis.ipynb` in a Jupyter Notebook runner such as VS Code
2. Take note of **ACTION**s
3. Run the python blocks
4. Observe the results and visualisations

## TO DOs

* Use a map projection library
* Use mean in location visualisations for consistency with other visualisations
* Preemptively merge all excecise types from exercise dataset
* Fine tune numerical correlation analysis to find significant correlations
* Use a more definitive calories burnt dataset
