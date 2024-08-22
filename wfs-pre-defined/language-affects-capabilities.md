# Language affects capabilities

**Purpose**: The user must be able to select one of the supported languages.
This language selection must be reflected in the provided capabilities document.

**Prerequisites**

* This test only applies to [Scenario 1](./README.md#scenarios) and [Scenario 2](./README.md#scenarios). Otherwise, the test case is skipped.
* [Provide Response Language](./provide-response-language)
* [Provide Supported Languages](./provide-supported-languages)

**Test method**

* Let the value of [GetCapabilities OnlineResource](#getcap-href) be ```getcapabilities-url```.
* Let the value of [SupportedLanguage codes](#supported-languages) be ```language-list```.
* For each ```language-list``` as ```lang-code```:
  * Create a GetCapabilities HTTP request by adding the parameters ```SERVICE=WFS```, ```REQUEST=GetCapabilities```, ```VERSION=2.0.0``` and ```LANGUAGE=``` + ```lang-code``` to the ```getcapabilities-url```
  * Execute the request. If the returned resource can be parsed as a valid XML document and if the document passes all the tests listed as prerequisites for this test:
    * Check that the [ResponseLanguage code](#response-language) equals the ```lang-code```. If it does not, fail the test for this language.
    * Check that the list of [SupportedLanguage codes](#supported-languages) equals ```language-list```. If not, fail the test for this language.
  * Otherwise fail the test.
* If the test for any of the languages failed, fail the test. Otherwise pass the test.

**Reference(s)**

* [TG DL] (./README.md#ref_TG_DL), Requirements 55, 56

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
SupportedLanguage codes <a name="supported-languages"></a>   | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities[1]/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language
ResponseLanguage code <a name="response-language"></a>   | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities[1]/inspire_common:ResponseLanguage/inspire_common:Language
GetCapabilities OnlineResource <a name="getcap-href"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:Operation[@name="GetCapabilities"]/ows:DCP/ows:HTTP/ows:Get[1]/@xlink:href
