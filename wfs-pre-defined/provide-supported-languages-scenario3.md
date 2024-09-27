# Provide Supported Languages - Scenario 3

**Purpose**: If the service supports several languages and there is no Extended Capabilities, the xml:lang attribute shall be used to define the languages used.

**Prerequisites**

* This test only applies to [Scenario 3](./README.md#scenarios). Otherwise, the test case is skipped.

**Test method**

* Check manually that if the service supports several languages and there is no Extended Capabilities, the _xml:lang_ attribute is used to define the languages used.

**Reference(s)**:

* [TG DL](./README.md#ref_TG_DL), Requirement 79

**Test type**: Manual

**Notes**

Example on the use of the _xml:lang_ attribute:

```xml
 <ows:ServiceIdentification>
      <ows:Title xml:lang="en">My WFS</ows:Title>
      <ows:Title xml:lang="da">Min WFS</ows:Title>
      <ows:Abstract xml:lang="en">My abstract</ows:Abstract>
      <ows:Abstract xml:lang="da">Min abstrakt</ows:Abstract>
      <ows:Keywords>
        <ows:Keyword xml:lang="en">My keyword</ows:Keyword>
        <ows:Keyword xml:lang="da">Mit emneord</ows:Keyword>
      </ows:Keywords>
      <ows:ServiceType>WFS</ows:ServiceType>
      <ows:ServiceTypeVersion>2.0.2</ows:ServiceTypeVersion>
      <ows:ServiceTypeVersion>2.0.1</ows:ServiceTypeVersion>
      <ows:ServiceTypeVersion>2.0.0</ows:ServiceTypeVersion>
      <ows:ServiceTypeVersion>1.1.0</ows:ServiceTypeVersion>
      <ows:ServiceTypeVersion>1.0.0</ows:ServiceTypeVersion>
      <ows:Fees>NONE</ows:Fees>
      <ows:AccessConstraints>NONE</ows:AccessConstraints>
   </ows:ServiceIdentification>
```

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
