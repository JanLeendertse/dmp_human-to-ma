# Human editable DMP to a maDMP

## Intention

The daily practise shows the demand for easy to understand templates for data management plans (DMP), which can be filled within know software packages. Those are mostly office tools like word processing or spread sheet software.

From the institutional point of view, DMPs produces with office tools lack interoperability. Information in word processing files or spread sheets is not easily transferable to solutions like „Research Data Management Organiser“ ([RDMO](https://github.com/rdmorganiser/rdmo)). The situation is even more complicated, because organization-wide solutions are not yet in production, but scientist already need DMPs in 2020.

## General idea

This project offers a pragmatic approach for scientist or research groups to generate a DMP with spreadsheet software, store it as a file, but add a script or macro that exports the entered data an a JSON file. The format of the JSON model proposed by „RDA DMP Common Standard for machine-actionable Data Management Plans“, which is available as [Github project](https://github.com/RDA-DMP-Common/RDA-DMP-Common-Standard).

The discussion about a standard for DMP did not come to an accepted consensus, but a short research showed the approach of the RDA DMP Common Standard as a feasible starting point. It will also be interoperable with RDMO.

## Technical base

The editable DMP should be available in OpenOffice format and Microsoft Office format. The conversion and export should be processed by internal scripting engines.

The development will start with LibreOffice, because I am more familiar with that.

## Content handling




# References

Software Project „DataStewards2“: https://github.com/datastewardstuw/DataStewards2
