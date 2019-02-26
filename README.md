# Task 1 (Multilingual Information Extraction) of CLEF eHealth 2019 

Please download our [training data from here](https://www.openagrar.de/receive/openagrar_mods_00046540?lang=en).

Run the script **evaluation.py** for the evaluation of the development set as shown below:

```
python3 evaluation.py --ids_file=<ids_file> --anns_file=<anns_file> --dev_file=<dev_file> --out_file=<out_file>
```

All four arguments are optional if using the default values **ids_development.txt**, **anns_train_dev.txt**, **dev.txt** and **output.txt**, respectively. The first two arguments (<ids_file> and <anns_file>) should the ones included in the training data zip file (**ids_development.txt** and **anns_train_dev.txt**, respectively). 

The predictions for the development set (<dev_file>) should have the following format:

```
13860	II
9932	II|C00-C97
8614
8630	XIII|M00-M25|M05-M14
```

Each line should start with the document id, followed by a TAB (if any prediciton is available for the document), and followed by the ICD-10 codes separated by the pipe symbol (|).

The output file (<out_file>, if default file) will inlude a record of all true positives, false positives and false negative, as well as the scores (precision, recall, f-score).




