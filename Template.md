# A Unique identification for this test

**Purpose**: One or two sentences inlined here: Why this test is necessary?

**Test method**

A paragraph of the for describing the test steps and assertions. Use bullets or any markdown formatting as necessary:

* Use the XPath abbreviations as links in the text: [ExtendedCapabilities](#extendedCapabilities) must exist...
* Step 2,...

**Reference(s)**: 

* References to the requirements. we should agree on abbreviations and collect them as a table in [README](http://inspire.ec.europa.eu/id/ats/download-wfs/3.1/README.md)

**Test type**: Automated or Manual

**Notes**

Any additional notes. We can also use this for open questions during drafting.

## Contextual XPath references

The namespace prefixes used as described in [README](http://inspire.ec.europa.eu/id/ats/download-wfs/3.1/README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="extendedCapabilities"></a>   | /wms:WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities[1]
