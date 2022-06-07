# Service Metadata

**Purpose**:
INSPIRE Metadata for the Download Service must EITHER be linked to via an [inspire_common:MetadataURL](#inspireCommonMetadataUrl) in an [ExtendedCapabilities](#ExtendedCapabilities) section, OR the [ExtendedCapabilities](#ExtendedCapabilities) section must contain all the INSPIRE Metadata for the Download Service in accordance with Table 19 and the inspire_dls:ExtendedCapabilities schema.

**Prerequisites**

* [Extended capabilities](http://inspire.ec.europa.eu/id/ats/download-wfs/3.1/wfs-pre-defined/extended-capabilities)

**Test method**

* Perform a GetCapabilities request
* Validate the Capabilities document to the XML schema at http://inspire.ec.europa.eu/schemas/inspire_dls/1.0/inspire_dls.xsd
* If a [inspire_common:MetadataURL](#inspireCommonMetadataUrl) is provided, request the Metadata document with this URL. Check if the response is a valid Metadata document.
  * If a inspire_common:MetadataURL is not provided, check manually that all mandatory metadata elements are present in the [ExtendedCapabilities](#ExtendedCapabilities) section in accordance to the mapping provided in Table 19 of the TG.

**Reference(s)**:

* [TG DL](http://inspire.ec.europa.eu/id/ats/download-wfs/3.1/wfs-pre-defined/README#ref_TG_DL), Requirement 53, Table 19

**Test type**:

Automated + Manual (if needed)

**Notes**

Table 19: Mapping INSPIRE Metadata elements to ISO 19142 WFS

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
