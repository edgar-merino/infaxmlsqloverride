

# INFA SQL Override

Given a valid exported XML INFA file, get those Source Qualifier transformations (and its hierarchy) where a SQL override has been specified and put this information into an excel file with the following information:

|Column|Value|
|--|--|
|Folder|Folder associated to the mapping|
|Mapping|Name of the mapping with the override sentence|
|Source Qualifier|Name of the Source Qualifier associated|
|Transformation type|Transformation type|
|SQL statement|Overrided SQL statement|


## Usage

`python getinfasqloverride.py <INFA_XML_FILE.xml>`

Where:

* INFA_XML_FILE.xml Valid INFA exported XML file to be processed

The progress will be shown:

```
Parsing <INFA_XML_FILE.xml> ...
Processing override SQL statements ...
Generating excel file: LAST_FOLDER.xlsx ...
Done
```

At the end of the process, a new Excel file will be generated with the same name as the last folder read from the INFA XML file.

### Notes

Due to Excel limitations, the max lenght for a cell is 32,767 characters. Queries larger than that will be truncated.

## Libraries

This program uses `lxml` to parse the input file and `openpyxl` to save the result on an Excel file.

## RST Links and references

- lxml: https://lxml.de/
- openpyxl: https://openpyxl.readthedocs.io/en/stable/

## Copyright & License

Copyright (c) 2021, Edgar Merino. MIT License.