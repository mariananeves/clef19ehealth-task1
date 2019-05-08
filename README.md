# Task 1 (Multilingual Information Extraction) of CLEF eHealth 2019 

Please download our [training data from here](https://www.openagrar.de/receive/openagrar_mods_00046540?lang=en) for the [Task 1 of the CLEF eHealth challenge](http://clef-ehealth.org/).

Run the script **evaluation.py** for the evaluation of the development set as shown below:

```
python3 evaluation.py --ids_file=<ids_file> --anns_file=<anns_file> --dev_file=<dev_file> --out_file=<out_file>
```

The script receives four arguments:

- ids_file: list of document ids of the development set, i.e. file **ids_development.txt** in the training data zip file
- anns_file: gold-standard annotations, i.e. file **anns_train_dev.txt** in the training data zip file
- dev_file: predictions for the development set (cf. format below)
- out_file: output file with evaluation (TP, FP, FP, precision, recall and f-score)

However, all four arguments are optional if using the default values **ids_development.txt**, **anns_train_dev.txt**, **dev.txt** and **output.txt**, respectively. 

The predictions for the development set (<dev_file>) should have the following format:

```
13860	II
9932	II|C00-C97
8614
8630	XIII|M00-M25|M05-M14
```

Each line should start with the document id. If any prediction is available for the document, the document id should be followed by a TAB and then by the ICD-10 codes separated by the pipe symbol (|). All documents from the development set should be included in the file, including the ones without any prediction. The order of the documents and the codes is not relevant.






