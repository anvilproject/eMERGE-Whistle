# eMERGE-Whistle
eMERGE Whistle projection files for transforming eMERGE dataset into FHIR

## Whistle
[Whistle](https://github.com/GoogleCloudPlatform/healthcare-data-harmonization) is a language developed for the purposes of transforming files from one form of JSON into another. For the purposes of ingesting eMERGE data into FHIR, we transform the CSV input into JSON objects and then tranform those into JSON suitable for passing the a FHIR REST Api endpoint. The language is concise and specific to this purpose and is therefore easy to read and not difficult to write. 

One of the strongest features built into Whistle is the use of FHIR [ConceptMaps](http://hl7.org/fhir/R4/conceptmap.html) to transform data from one terminology to another easily. This is a core aspect of the data harmonization part of the system's name and is central to the language itself. 

## Pipeline
We are working on a python application that will convert simple CSV files into the necessary ConceptMaps and JSON input as well as automate the whistle process itself. While many datasets will conform to similar enough formats that a single whistle projector will suffice for many datasets, there will likely be a need to write separate projectors for each of the different groups. So, this particular projection library will not work well with CMG or INCLUDE, but could be used as a starting point. 
