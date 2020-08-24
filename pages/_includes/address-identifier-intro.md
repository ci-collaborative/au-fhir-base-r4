**Extension: Address Identifier** *[[FMM Level 0](guidance.html)]*

This extension applies to the Address datatype and is used to represent an identifier for an address. 

An address identifier does not form part of the address itself, e.g. a street number. It is a unique identifier associated with a location address and may be used to look up an address, validate an address, or link to other data relating to an address.

#### Identifiers
These definitions, defined as profiles of [Identifier](http://hl7.org/fhir/R4/datatypes.html#Identifier), represent common identifiers that may be sent using this extension:
* [Delivery Point Identifier](StructureDefinition-au-deliverypointidentifier.html)
* [G-NAF Identifier](StructureDefinition-au-gnafidentifier.html)


**Examples**

[Postal address (with DPID and G-NAF Identifier) and work address in Darwin, NT](Patient-address-example0-identifiers.html)