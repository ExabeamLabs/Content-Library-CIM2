#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-file-edreventcategory
  ParserVersion = "v1.0.0"
  ExtractionType = json
  Conditions = [ """"dataSource.name":"SentinelOne"""",  """"event.category":"file"""", """"event.type":""" ]
  DupFields = [ "host->dest_host"]


}
```