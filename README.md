# Google-Ads-Database
Google is a multinational technology company offering online advertising services through the Google Ads platform. As a data analyst, you have been tasked with developing a comprehensive Relational Database Management System (RDBMS) to support Google Ads operations.The goal is to manage advertisers, campaigns, ads, keywords, and performance metrics

## Objectives
* Identifying the main entities in the database system.
* Clearly defining the attributes, relationships and constraint that support the business needs.
* Designing an entity relationship diagram that supports the business needs based on the database entities, relatinships and participation constraints.


  
## Main Entities in the table
Entities are tables or real world objects that are meant to store information in the database. They are fundamental component of an Entity Relationship Diagram(ERD).

# Advertiser
This is the table that stores the advertisers' information. The attributes and data types are as follows:<br>
AdvertiserID **INT** PK <br>
AdvertiserName **VARCHAR**<br>
ContactPerson **VARCHAR**<br>
ContactEmail **VARCHAR**<br>

## Campaign
This is the table that stores information from the campaigns. The attributes and data types are as follows:<br>
CampaignID **INT** PK <br>
AdvertiserID **INT** FK <br>
CampaignName **VARCHAR**<br>
StartDate **DATE**<br>

## Advertisement
This is the table that stores information from the advertisement. The attributes and data types are as follows:<br>
AdID **INT** PK <br>
CampaignID **INT** FK <br>
AdTitle **VARCHAR**<br>
TargetURL **VARCHAR**<br>
Impression **SMALLINT**<br>

## Keyword
This is the table that stores information from keyword. The attributes and data types are as follows:<br>
KeywordID **INT** PK <br>
AdID **INT** FK <br>
KeywordText **TEXT**<br>
BidAmount **SMALLINT**<br>
QualityScore **SMALLINT**<br>

## Performance
This is the table that stores information from performance.  The attributes and data types are as follows:<br>
PerformanceID **INT** PK <br>
AdID **INT** FK <br>
Date **DATE**<br>
Clicks **SMALLINT**<br>
Conversions **SMALLINT**<br>

## The Cardinality and Requirements For The Database
Advertiser - Campaign: One advertiser can manage multiple campaigns, but each campaign belongs to a single advertiser. (one-to-many)
Campaign – Ad: One campaign can contain multiple ads, but each ad is linked to one campaign. (one-to-many)
Ad - Keyword: An ad can target multiple keywords, but each keyword is associated with one ad. (one-to-many)
Ad - Performance: One ad can generate multiple performance records over time, but each performance record belongs to a specific ad. (one-to-many)

## The Entity Relationship Diagram
The Entity Relationship Diagram shoes the collection of objects within a database and the relationships between them. It included the entities, schemas, participation,
constraint avd the relationships between the entities. I modelled this using the ERD tools by defining the table and specifying the relationships between the tables using
pre-existing columns as foriegn keys.
