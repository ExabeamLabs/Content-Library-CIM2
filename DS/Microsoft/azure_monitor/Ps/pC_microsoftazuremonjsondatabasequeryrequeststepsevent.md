#### Parser Content
```Java
{
Name = microsoft-azuremon-json-database-query-requeststepsevent
  Product = Azure Monitor
  ParserVersion = v1.0.0
  ExtractionType = json
  Conditions = [ """"resourceId":""", """"category":"RequestSteps"""", """"operationName":"RequestStepsEvent"""" ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
    """"StartTime":"({time}\d\d\d\d\-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$..Command,exa_field_name=db_query""",
  ]


}
```