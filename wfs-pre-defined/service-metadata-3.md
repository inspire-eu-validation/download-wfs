# Service Metadata - Scenario 3

**Purpose**: The capabilities section of the Download Service contains the Download Service metadata elements in accordance with Table 19b.

**Prerequisites**

This test only applies to [Scenario 3](./README.md#scenarios). Otherwise, the test case is skipped.

**Test method**

* Perform a GetCapabilities request
* Validate the Capabilities document to the XML schema at ......
* Check that all mandatory metadata elements are present in the Capabilities section in accordance to the mapping provided in Table 19b of the TG.

**Reference(s)**:

* [TG DL](./README.md#ref_TG_DL), Requirement 53 (3)

**Test type**:

Automated

**Notes**

Table 19b: Mapping INSPIRE Metadata elements to ISO 19142 WFS without extended capabilities

INSPIRE Metadata elements<br>[Mandatory (M) - Conditional (C)] |ISO 19142 elements of<br><WFS\_Capabilities>
--------------------------------------------------- | -------------------------------------------------------------------------
|Resource Title (M) |ows:ServiceIdentification/ows:Title |
|Resource Abstract (M) |ows:ServiceIdentification/ows:Abstract |
|Resource Type (M) |inspire\_common:ResourceType (ExtendedCapabilities) |
|Resource Locator (C) |inspire\_common:ResourceLocator (ExtendedCapabilities) |
|Coupled Resource (C) |wfs:MetadataURL (per feature type) |
|Spatial Data Service Type (M) |inspire\_common:SpatialDataServiceType (ExtendedCapabilities) |
|Keyword (M) |ows:Keywords/ows:Keyword; inspire\_common:Keyword |
|Geographic Bounding Box (M) |ows:WGS84BoundingBox (Layer property) |
|Temporal Reference (M) |inspire\_common:TemporalReference (ExtendedCapabilities) |
|Spatial Resolution (C) |ows:ServiceIdentification/ows:Abstract |
|<p>Conformity\* (M) </p><p>\*refers to conformity of to the Data Specificaitons </p>|inspire\_common:Conformity (ExtendedCapabilities) |
|Conditions for Access and Use (M) |ows:ServiceIdentification/ows:Fees |
|Limitations on Public Access (M) |ows:ServiceIdentification/ows:AccessConstraints|
|Responsible Organisation (M) |<p>ows:ServiceProvider/ows:ProviderName and: </p><p>ows:ServiceProvider/ows:ServiceContact/ows:ContactInfo </p>|
|Metadata Point of Contact (M) |inspire\_common:MetadataPointOfContact (ExtendedCapabilities) |
|Metadata Date (M) |inspire\_common:MetadataDate (ExtendedCapabilities) |
|Metadata Language (M) |inspire\_common:SupportedLanguages (ExtendedCapabilities) |
|Unique Resource Identifier (M) |<p>inspire\_dls:SpatialDataSetIdentifier/inspire\_common:Code </p><p>inspire\_dls:SpatialDataSetIdentifier/inspire\_common:Namespace </p><p>(ExtendedCapabilities) </p>|




## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/download-wfs/3.1/wfs-pre-defined/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="ExtendedCapabilities"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/
inspire_common:MetadataURL <a name="inspireCommonMetadataUrl"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:MetadataUrl/inspire_common:URL
