# **NF-kBIn**
A computational approach to predict the NF-kB inhibitors using the SMILES information of the molecules.
## Introduction
NF-kBIn is developed to predict the NF-kB inhibitors using the SMILES information of the molecules. In the standalone version, support vector classifier based model is implemented.
NF-kBIn is also available as web-server at https://webs.iiitd.edu.in/raghava/nfkbin. Please read/cite the content about the NF-kBIn for complete information including algorithm behind the approach.

## datasets folder
Contain all the datasets

## Standalone
The Standalone version of NF-kBIn is written in python3 and following libraries are necessary for the successful run:
- scikit-learn
- Pandas
- Numpy
- openbabel (http://openbabel.org/docs/index.html)
- PaDEL-Descriptor (http://yapcwsoft.com/dd/padeldescriptor/PaDEL-Descriptor.zip)

## Minimum USAGE
To know about the available option for the stanadlone, type the following command:
```
python nfkbin.py -h
```
To run the example, type the following command:
```
python3 nfkbin.py -i example_input.txt
```
This will predict if the submitted molecules are NF-kB inhibitors or not. It will use other parameters by default. It will save the output in "outfile.csv" in CSV (comma seperated variables).

## Full Usage
```
usage: nfkbin.py [-h] 
                       [-i INPUT 
                       [-o OUTPUT]
		       [-t THRESHOLD]
		       [-d {1,2}]
```
```
Please provide following arguments for successful run

optional arguments:
  -h, --help            show this help message and exit
  -i INPUT, --input INPUT
                        Input: Moleculues in the SMILES format per line
  -o OUTPUT, --output OUTPUT
                        Output: File for saving results by default outfile.csv
  -t THRESHOLD, --threshold THRESHOLD
                        Threshold: Value between 0 to 1 by default 0.41
  -d {1,2}, --display {1,2}
                        Display: 1:NF-kB inhibitors only, 2: All molecules, by default 1
```

**Input File:** It allow users to provide input in the SMILES format.

**Output File:** Program will save the results in the CSV format, in case user do not provide output file name, it will be stored in "outfile.csv".

**Threshold:** User should provide threshold between 0 and 1, by default its 0.16.

**Display type:** This option allow users to fetch either only NF-kB inhibitors by choosing option 1 or prediction against all molecules by choosing option 2.

NF-kBIn Package Files
=======================
It contantain following files, brief descript of these files given below

INSTALLATION                    : Installations instructions

LICENSE                         : License information

README.md                       : This file provide information about this package

model.zip                       : This zipped file contains the compressed version of model

nfkbin.py                       : Main python program

example_input.txt               : Example file contain molecules in SMILES format

example_output.csv              : Example output file
