# Human editable DMP to a maDMP

## Intention

The daily practise shows the demand for easy to understand templates for data management plans (DMP), which can be filled within know software packages. Those are mostly office tools like word processing or spread sheet software.

From the institutional point of view, DMPs produces with office tools lack interoperability. Information in word processing files or spread sheets is not easily transferable to solutions like „Research Data Management Organiser“ ([RDMO](https://github.com/rdmorganiser/rdmo)). The situation is even more complicated, because organization-wide solutions are not yet in production, but scientist already need DMPs in 2020.

## General idea

This project offers a pragmatic approach for scientist or research groups to generate a DMP with spreadsheet software, store it as a file, but add a script or macro that exports the entered data an a JSON file. The format of the JSON model proposed by „RDA DMP Common Standard for machine-actionable Data Management Plans“ (RDA-DMP), which is available as [Github project](https://github.com/RDA-DMP-Common/RDA-DMP-Common-Standard).

The discussion about a standard for DMP did not come to an accepted consensus, but a short research showed the approach of the RDA DMP Common Standard as a feasible starting point. It will also be interoperable with RDMO.

## Technical base

The editable DMP should be available at least in OpenOffice format and Microsoft Office format. The conversion and export should be processed by internal scripting engines.

The development will start with LibreOffice, because I am more familiar with that.

The output should fit into the RDA-DMP structure. Version 1.0 is published on [Github](https://github.com/RDA-DMP-Common/RDA-DMP-Common-Standard/blob/master/examples/JSON/JSON-schema/1.0/maDMP-schema-1.0.json).

## Content handling by users

The spreadsheet must contain all fields used in RDA-DMP. It should display explainations and guidings to reduce the investigation efforts while working with the template.

Entering data into a sheet must be possible with the only knowledge how to work with spreadsheet software.

The answers of the researchers are stored as spreadsheet file and can be sent around in that format.

## Exporting

The other role is to export data if a JSON object of the stored answers is wanted. The person acting as exporter must know how to start the export script and to process the exported JSON dataset.

There might be two approaches:

1. The script for generating a JSON dataset is stored in the spreadsheet template and can be start from the file itself.
2. The spreadsheet file uses labels for the answer sections, which can be processed by external scripts.

## Security issues

Usually, macros or internal scripts are recognized as a security issue, because it is the main attack vector. The conditions of processing should be explicated to allow official and functioning workflows. It should be possible for organisations to add certificates to the software, that can be parsed. If exporting approach 2. is implemented, this issue might not be that prevalent. But then two different pieces of software – template for entering user data and script file for processing user data – must be handled.


# References

Software Project „DataStewards2“: https://github.com/datastewardstuw/DataStewards2
