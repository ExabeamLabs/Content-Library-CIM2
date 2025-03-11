#### Parser Content
```Java
{
Name = microsoft-azuremon-json-app-activity-success-errors
  Product = Azure Monitor
  ParserVersion = v1.0.0
  Conditions = [
    """"resourceId":""",
    """"category":"Errors"""",
    """"operationName":"ErrorEvent""""
  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
	  """"DatabaseName":"({db_name}[^"]+)""""
  ]


}
```