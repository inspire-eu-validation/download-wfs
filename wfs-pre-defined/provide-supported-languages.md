# Provide Supported Languages

**Purpose**: The Capabilities document must contain a list of supported languages

**Prerequisites**

* This test only applies to [Scenario 1](./README.md#scenarios) and [Scenario 2](./README.md#scenarios). Otherwise, the test case is skipped.

**Test method**

* Check that the [Supported language codes](#supported-languages) list is non-empty. If so, pass the test. Otherwise fail the test.

**Reference(s)**:

* [TG DL](./README.md#ref_TG_DL), Requirement 59

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Supported language codes <a name="supported-languages"></a>   | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities[1]/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language
