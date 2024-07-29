# Service Metadata - Scenario 1

**Purpose**: Test that the [ExtendedCapabilities](#ExtendedCapabilities) section of the Download Service is in accordance with the schema at https://inspire.ec.europa.eu/schemas/inspire_dls/1.0/inspire_dls.xsd and contains a link to the metadata record of the service in an INSPIRE Discovery catalogue in element [inspire_common:MetadataURL](#inspireCommonMetadataUrl).

**Prerequisites**

This test only applies to Scenario 1. Otherwise the test case is skipped.


**Test method**

* Perform a GetCapabilities request
* Validate the Capabilities document to the XML schema at http://inspire.ec.europa.eu/schemas/inspire_dls/1.0/inspire_dls.xsd
* If a [inspire_common:MetadataURL](#inspireCommonMetadataUrl) is provided, request the Metadata document with this URL. Check if the response is a valid Metadata document.

**Reference(s)**:

* [TG DL](./README.md#ref_TG_DL), Requirement 53 (1)

**Test type**:

Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-wfs/3.1/wfs-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="ExtendedCapabilities"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/
inspire_common:MetadataURL <a name="inspireCommonMetadataUrl"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:MetadataUrl/inspire_common:URL
