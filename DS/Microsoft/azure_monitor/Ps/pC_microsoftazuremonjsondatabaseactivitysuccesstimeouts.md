#### Parser Content
```Java
{
Name = microsoft-azuremon-json-database-activity-success-timeouts
  Product = Azure Monitor
  ParserVersion = v1.0.0
  Conditions = [
    """"resourceId":""",
    """"category":"Timeouts"""",
    """"operationName":"TimeoutEvent""""
  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
	  """"DatabaseName":"({db_name}[^"]+)""""
  ]


}
```