# Towards-End-User-Development-for-IoT

The current repository hosts the data was used in the paper "Towards End-User Development for IoT: A Case Study on Semantic Parsing of Cooking Recipes for Programming Kitchen Devices".

Firstly, in the annotation guidelines, `annotation_guidelines.md`, are the practises that the annotator should follow. Also, there is a table of listed events that were used in the study.

Next is listed the `kitchen_appliance_dictionary.json` dictionary which was used to retrieve recipes that mention an oven or a fridge or a subclass of them.

Lastly, inside the `data` directory are listed the datasets for the oven taking into account all the events (see the table in, `annotation_guidelines.md`), then for the fridge with all the events found and for the oven with only the type 1 event, for more details see into the paper.

Inside each, you can find a stratified train-valid-test dataset split. It uses the IOB format, similarly to the CoNLL-2003 dataset, but has only three columns:
- token
- POS tag provided by the spaCy library
- label

The label, according to the paper, can be: "where", "what", "why" and "how". 



#### Project Organization

------------
    ├── annotation_guidelines.md           <- Annotation Guidelines
    ├── data
    │   ├── fridge                         <- The IOB stratified dataset split for the fridge
    │   │   ├── test.txt
    │   │   ├── train.txt
    │   │   └── valid.txt
    │   ├── oven                           <- The IOB stratified dataset split for the oven
    │   │   ├── test.txt
    │   │   ├── train.txt
    │   │   └── valid.txt
    │   └── oven_type_1                    <- The IOB stratified dataset split for only the event
    │                                           type 1 of the oven
    │       ├── test.txt
    │       ├── train.txt
    │       └── valid.txt
    ├── kitchen_appliance_dictionary.json  <- The dictionary used to retrieve recipes which use 
    │                                           the "oven" and the "fridge"
    ├── LICENSE
    └── README.md                          <- YOU ARE HERE
--------