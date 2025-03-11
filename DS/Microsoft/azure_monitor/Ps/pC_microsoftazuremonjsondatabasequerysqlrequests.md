#### Parser Content
```Java
{
Name = microsoft-azuremon-json-database-query-sqlrequests
  Product = Azure Monitor
  ParserVersion = v1.0.0
  Conditions = [ """"resourceId":""", """"category":"SqlRequests"""", """"operationName":"SqlRequestsEvent"""" ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
    """exa_json_path=$..Command,exa_field_name=db_query""",
    """"properties".+?Command":"({db_query}[^"]+)","""
    """"StartTime":"({time}\d\d\d\d\-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  ]


}
```