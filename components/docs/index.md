# Welcome to MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## xsd

```
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema" xmlns:tns="http://mapservices.prorail.nl/storingen/schema/geocoderen_2" targetNamespace="http://mapservices.prorail.nl/storingen/schema/geocoderen_2" elementFormDefault="qualified" attributeFormDefault="unqualified" version="1">
	<xs:element name="GeocodePunten" type="tns:GeocodePunten_Type"/>
	<xs:complexType name="GeocodePunten_Type">
		<xs:sequence>
			<xs:element name="Name" type="xs:string" default="JSONFeatue" minOccurs="1" maxOccurs="1">
				<xs:annotation>
					<xs:documentation>Name of the feature</xs:documentation>
				</xs:annotation>
			</xs:element>
			<xs:element name="Type" type="xs:string" default="GeocodePunten" minOccurs="1" maxOccurs="1">
				<xs:annotation>
					<xs:documentation>Type of feature</xs:documentation>
				</xs:annotation>
			</xs:element>
			<xs:element name="Features" type="tns:Feature_Type" minOccurs="1" maxOccurs="unbounded"/>
		</xs:sequence>
	</xs:complexType>
	<xs:complexType name="Feature_Type">
		<xs:sequence>
			<xs:element name="Geocode" type="xs:string" minOccurs="1" maxOccurs="1">
				<xs:annotation>
					<xs:documentation>Geocode value.</xs:documentation>
				</xs:annotation>
			</xs:element>
			<xs:element name="Geometry" type="tns:Geometry_Type" minOccurs="1" maxOccurs="1"/>
			<xs:element name="Properties" type="tns:Properties_Type" minOccurs="1" maxOccurs="1"/>
		</xs:sequence>
	</xs:complexType>
	<xs:complexType name="Geometry_Type">
		<xs:sequence>
			<xs:element name="Type" type="xs:string" minOccurs="1" maxOccurs="1">
				<xs:annotation>
					<xs:documentation>Type of geometry</xs:documentation>
				</xs:annotation>
			</xs:element>
			<xs:element name="CoordinatesRD" type="tns:Punten_Type" minOccurs="2" maxOccurs="2"/>
			<xs:element name="CoordinatesWGS" type="tns:Punten_Type" minOccurs="2" maxOccurs="2">
				<xs:annotation>
					<xs:documentation>Coordinates in WGS system</xs:documentation>
				</xs:annotation>
			</xs:element>
		</xs:sequence>
	</xs:complexType>
	<xs:complexType name="Properties_Type">
		<xs:sequence>
			<xs:element name="Punten" type="tns:Punten_Type" minOccurs="1" maxOccurs="unbounded"/>
			<xs:element name="PartitionKey" type="xs:string" minOccurs="1" maxOccurs="1">
				<xs:annotation>
					<xs:documentation>Partition key value</xs:documentation>
				</xs:annotation>
			</xs:element>
		</xs:sequence>
	</xs:complexType>
	<xs:complexType name="Punten_Type">
		<xs:sequence>
			<xs:element name="Punt" type="xs:float" default="0" minOccurs="1" maxOccurs="1">
				<xs:annotation>
					<xs:documentation>Punten value</xs:documentation>
				</xs:annotation>
			</xs:element>
		</xs:sequence>
	</xs:complexType>
</xs:schema>
```



## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
## demoootje
demo

#### linkjes
[links](details/component01.md)

## Tutorial  

This is my tutorial..
![alt text](testje.drawio)

### images

![Alt Text](LCM-cycles.png)

# Person

## Properties

- **`firstName`** *(string)*: The person's first name.
- **`lastName`** *(string)*: The person's last name.
- **`age`** *(integer)*: Age in years which must be equal to or greater than zero. Minimum: `0`.
