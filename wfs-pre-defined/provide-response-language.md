# Provide Response Language

**Purpose**: The Capabilities document must contain the response language

**Prerequisites**

* This test only applies to [Scenario 1](./README.md#scenarios) and [Scenario 2](./README.md#scenarios). Otherwise, the test case is skipped.

**Test method**

* Check that [ResponseLanguage](#responseLanguage) exists. If so, pass the test. Otherwise fail the test.

**Reference(s)**:

* [TG DL](./README.md#ref_TG_DL), Requirement 58

**Test type**:

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ResponseLanguage <a name="responseLanguage"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:ResponseLanguage/inspire_common:Language
