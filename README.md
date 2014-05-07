# NOMIS / ODC Project

This is a proof-of-concept for integrating data from the NOMIS API with data from the Open Data Communities project. Normal service will be resumed shortly.

## Structure of NOMIS Queries

1. Datasets can be accessed as [html](https://www.nomisweb.co.uk/api/v01/dataset/NM_618_1/def.htm), csv or json. 
2. The structure of URIs is (more or less) the same, but if you get stuck, the html explorer (see point one) can point you in the right direction. 
3. Codes for geography, sex etc are needed to narrow down datasets to return results. When requesting CSVs, omitting these returns the full dataset (up to 25000 rows without an API key); when requesting JSON, more specific queries are required.

## Useful Links on NOMIS

1. API Documentation [here](https://www.nomisweb.co.uk/api/v01/help).
2. AJAX Example [here](http://www.nomisweb.co.uk/websvc/examples/ajax_json.htm). Click 'view source' to see developer comments on the querying steps taken to return results.
3. The html page for the dataset we're interested in is [here](https://www.nomisweb.co.uk/api/v01/dataset/NM_618_1/def.htm).

### Examples pinched directly from NOMIS documentation: 

#### Example (XML):
- [What top level areas are available?](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/geography.def.sdmx.xml)
- [What areas are within Darlington?](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/geography/2038432081.def.sdmx.xml)
- [Partial codelist of the wards in Darlington](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/geography/2038432081TYPE1.def.sdmx.xml)
- [Search for wards ending with "central" in Darlington](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/geography/2038432081TYPE1.def.sdmx.xml?search=*central)
- [List all available genders ("sex") from the "Claimant Count with Rates and Proportions" dataset after selecting geography](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/sex.def.sdmx.xml?geography=2038432081)
- [List all available items ("item") from the "Claimant Count with Rates and Proportions" dataset after selecting geography and sex](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/item.def.sdmx.xml?geography=2038432081&sex=7)
- [Display metadata about the date January 2010](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/time/2010-01.metdata.xml)
- [Display metadata about the all dates including dates that are yet to be released](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/time.metdata.xml)

#### Example (JSON):
- [What top level areas are available?](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/geography.def.sdmx.json)
- [What areas are within Darlington?](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/geography/2038432081.def.sdmx.json)
- [Partial codelist of the wards in Darlington](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/geography/2038432081TYPE1.def.sdmx.json)
- [Search for wards ending with "central" in Darlington](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/geography/2038432081TYPE1.def.sdmx.json?search=*central)
- [List all available genders ("sex") from the "Claimant Count with Rates and Proportions" dataset after selecting geography](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/sex.def.sdmx.json?geography=2038432081)
- [List all available items ("item") from the "Claimant Count with Rates and Proportions" dataset after selecting geography and sex](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/item.def.sdmx.json?geography=2038432081&sex=7)
- [Display metadata about the date January 2010](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/time/2010-01.metdata.json)
- [Display metadata about the all dates including dates that are yet to be released](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/time.metdata.json)

#### Example (HTML):
- [What top level areas are available?](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/geography.def.htm)
- [What areas are within Darlington?](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/geography/2038432081.def.htm)
- [Partial codelist of the wards in Darlington](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/geography/2038432081TYPE1.def.htm)
- [Search for wards ending with "central" in Darlington](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/geography/2038432081TYPE1.def.htm?search=*central)
- [List all available genders ("sex") from the "Claimant Count with Rates and Proportions" dataset after selecting geography](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/sex.def.htm?geography=2038432081)
- [List all available items ("item") from the "Claimant Count with Rates and Proportions" dataset after selecting geography and sex](https://www.nomisweb.co.uk/api/v01/dataset/NM_1_1/item.htm?geography=2038432081&sex=7)