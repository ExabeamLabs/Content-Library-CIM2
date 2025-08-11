#### Parser Content
```Java
{
Name = microsoft-azuremon-json-endpoint-activity-success-catchall
   TimeFormat = [ "M/d/yyyy H:mm:ss.SSS"]
   ParserVersion = v1.0.0
   Conditions = [ """destinationServiceName =Azure""" , """ResourceId":"""" , """"category":"""" ]
   Fields = ${MSParserTemplates.microsoft-azure-endpoint-json.Fields}[
    """exa_regex=eventTimestamp":"({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+.\d\d\d)"""
  ]
 

}
```