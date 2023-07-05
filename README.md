![Exabeam](https://user-images.githubusercontent.com/57500390/233131296-b8618125-ef0d-497b-9c50-a8abe8b0d2b4.svg)

# Exabeam Content Library - New-Scale
Based on the Common Information Model 2.0

Welcome to the Exabeam New-Scale Content Library.

The New-Scale Content Library is an online repository of knowledge and content that organizations can use to learn about available log source integrations and security use cases.

This library reflects the hierarchical framework of the Exabeam Common Information Model. The library is programmaticly generated  from the Exabeam content repository. As changes are made to the information model, or new content is added to the content repository, the New-Scale Content Library is automatically updated to provide fast and easy access.
 
 * If you are using earlier versions of Advanced Analytics, see the [Content Library](https://github.com/ExabeamLabs/Content-Doc).

## Content

|Branch|Version|Content|MITRE ATT&CK®|Release Notes
|--|--|--|--|--|
|master|canary|[Data Sources](Exabeam%20Data%20Sources.md), [Use Cases](Exabeam%20Use%20Cases.md), [Product Categories](Exabeam%20Product%20Categories.md)|[Coverage Map](https://mitre-attack.github.io/attack-navigator/#layerURL=https://raw.githubusercontent.com/ExabeamLabs/Content-Library-CIM2/master/resources/mitre_map.json)|
|c2206.2_97_63.5|I63.5|[Data Sources](https://github.com/ExabeamLabs/Content-Library-CIM2/blob/c2206.2_97_63.5/Exabeam%20Data%20Sources.md), [Use Cases](https://github.com/ExabeamLabs/Content-Library-CIM2/blob/c2206.2_97_63.5/Exabeam%20Use%20Cases.md), [Product Categories](https://github.com/ExabeamLabs/Content-Library-CIM2/blob/c2206.2_97_63.5/Exabeam%20Product%20Categories.md)|[Coverage Map](https://mitre-attack.github.io/attack-navigator/#layerURL=https://raw.githubusercontent.com/ExabeamLabs/Content-Library-CIM2/c2206.2_97_63.5/resources/mitre_map.json)|[Release Notes](https://github.com/ExabeamLabs/Content-Library-CIM2/blob/c2206.2_97_63.5/ReleaseNotes/ReleaseNotes_c2206.2_97_63.5.md)
|c2206.2_63_4_adap|I63.4|[Data Sources](https://github.com/ExabeamLabs/Content-Library-CIM2/blob/c2206.2_63_4_adap/Exabeam%20Data%20Sources.md), [Use Cases](https://github.com/ExabeamLabs/Content-Library-CIM2/blob/c2206.2_63_4_adap/Exabeam%20Use%20Cases.md), [Product Categories](https://github.com/ExabeamLabs/Content-Library-CIM2/blob/c2206.2_63_4_adap/Exabeam%20Product%20Categories.md)|[Coverage Map](https://mitre-attack.github.io/attack-navigator/#layerURL=https://raw.githubusercontent.com/ExabeamLabs/Content-Library-CIM2/c2206.2_63_4_adap/resources/mitre_map.json)

[Correlation Rule Templates](Exabeam%20Correlation%20Rules.md) – A list of prebuilt supported correlation rules with descriptions and use cases

[Platforms and Landscapes](https://github.com/ExabeamLabs/CIMLibrary/blob/main/Platforms_Landscapes.md) – A list of platforms listed by landscape (redirects to Common Information Model Library)

[Field Descriptions](https://github.com/ExabeamLabs/CIMLibrary/blob/main/Fields_Descriptions.md) – A list of available fields and their descriptions (redirects to Common Information Model Library)


## How do I use it? 

The New-Scale Content Library contains information about parsers, events, models, and rules. It shows what content is available and how the content elements map to one and other. To use the library, find your version of Advanced Analytics and drill into the information in one of the following ways: 

- <b>Data Sources</b> – Click Data Sources and select a vendor and a product that are the source of specific data. View the activity types, the parsers, and the number of rules and models Exabeam employs to cover this data source. Drill down further to view the parser syntax or the names of the rules and models. 

- <b>Use Cases</b> – Click Use Cases and select a specific use case. Exabeam supports use cases in the following categories: compromised insiders, malicious insiders, and external threats. View tables for each vendor and product that the use case supports. Each table shows the relevant activity types, parsers, and the number of supported rules and models. Drill down further to view the names of the rules and models. 

- <b>Product Categories</b> – Click Product Categories to view a list of products arranged by categories. Select a product to view the activity types, parsers, and the number of rules and models Exabeam employs to cover this data source. Drill down further to view the parser syntax or the names of the rules and models. 

- <b>MITRE ATT&CK®</b> - Click Coverage Map to view the attack techniques Exabeam covers with its rules and models.


The New-Scale Content Library also includes a list of prebuilt correlation rules. In addition, you can browse other resources to understand how the library is based on the Common Information Model 2.0, including a list of platforms and landscapes and a list of field descriptions. 

## How can it help me?
The New-Scale Content Library helps answer some of the most frequently asked questions regarding Exabeam's rich security content:

 - What use cases does Exabeam content support out of the box?
   - What are the data sources that can be used to get that content to function? 
   - What are the components of Exabeam content that enable that use case?

 - What data sources does Exabeam support out of the box?
   - What use case(s) does that content enable?
   - What are the components of Exabeam content that are enabled by a data source integration?
