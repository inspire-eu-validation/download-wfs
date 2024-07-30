# Service Metadata - Scenario 2

**Purpose**: The [ExtendedCapabilities](#ExtendedCapabilities) section of the Download Service is in accordance with the schema at https://inspire.ec.europa.eu/schemas/inspire_dls/1.0/inspire_dls.xsd and contains a link to the metadata record of the service in an INSPIRE Discovery catalogue in element [inspire_common:MetadataURL](#inspireCommonMetadataUrl)
Test that the capabilities section and the ExtendedCapabilities](#ExtendedCapabilities) section of the Download Service contain the Download Service metadata elements in accordance with Table 19a, in accordance with the schema at at https://inspire.ec.europa.eu/schemas/inspire_dls/1.0/inspire_dls.xsd.


**Prerequisites**

This test only applies to [Scenario 2](./README.md#scenarios). Otherwise, the test case is skipped.

**Test method**

* Perform a GetCapabilities request
* Validate the Capabilities document to the XML schema at http://inspire.ec.europa.eu/schemas/inspire_dls/1.0/inspire_dls.xsd
* Check that all mandatory metadata elements are present in the ExtendedCapabilities section in accordance to the mapping provided in Table 19a of the TG.

**Reference(s)**:

* [TG DL](./README.md#ref_TG_DL), Requirement 53 (1)

**Test type**:

Automated

**Notes**

Table 19a: Mapping INSPIRE Metadata elements to ISO 19142 WFS with extended capabilities

INSPIRE Metadata elements<br>[Mandatory (M) - Conditional (C)] |ISO 19142 elements of<br><WFS\_Capabilities>
--------------------------------------------------- | -------------------------------------------------------------------------
|Resource Title (M)                                 |ows:ServiceIdentification/ows:Title |
|Resource Abstract (M)                              |ows:ServiceIdentification/ows:Abstract |
|Resource Type (M)                                  |inspire\_common:ResourceType (ExtendedCapabilities) |
|Resource Locator (C)                               |inspire\_common:ResourceLocator (ExtendedCapabilities) |
|Coupled Resource (C)                               |wfs:MetadataURL (per feature type) |
|Spatial Data Service Type (M)                      |inspire\_common:SpatialDataServiceType (ExtendedCapabilities) |
|Keyword (M)                                        |ows:Keywords/ows:Keyword; inspire\_common:Keyword |
|Geographic Bounding Box (M)                        |ows:WGS84BoundingBox (Layer property) |
|Temporal Reference (M)                             |inspire\_common:TemporalReference (ExtendedCapabilities) |
|Spatial Resolution (C)                             |ows:ServiceIdentification/ows:Abstract |
|<p>Conformity\* (M) </p><p>\*refers to conformity of to the Data Specificaitons </p>|inspire\_common:Conformity (ExtendedCapabilities) |
|Conditions for Access and Use (M)                  |ows:ServiceIdentification/ows:Fees |
|Limitations on Public Access (M)                   |ows:ServiceIdentification/ows:AccessConstraints|
|Responsible Organisation (M)                       |<p>ows:ServiceProvider/ows:ProviderName and: </p><p>ows:ServiceProvider/ows:ServiceContact/ows:ContactInfo </p>|
|Metadata Point of Contact (M)                      |inspire\_common:MetadataPointOfContact (ExtendedCapabilities) |
|Metadata Date (M)                                  |inspire\_common:MetadataDate (ExtendedCapabilities) |
|Metadata Language (M)                              |inspire\_common:SupportedLanguages (ExtendedCapabilities) |
|Unique Resource Identifier (M)                     |<p>inspire\_dls:SpatialDataSetIdentifier/inspire\_common:Code </p><p>inspire\_dls:SpatialDataSetIdentifier/inspire\_common:Namespace </p><p>(ExtendedCapabilities) </p>|




## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-wfs/3.1/wfs-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="ExtendedCapabilities"></a>   | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/
inspire_common:MetadataURL <a name="inspireCommonMetadataUrl"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:MetadataUrl/inspire_common:URL
