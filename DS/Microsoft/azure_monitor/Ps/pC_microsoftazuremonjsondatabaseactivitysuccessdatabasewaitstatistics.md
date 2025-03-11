#### Parser Content
```Java
{
Name = microsoft-azuremon-json-database-activity-success-databasewaitstatistics
  Product = Azure Monitor
  ParserVersion = v1.0.0
  Conditions = [
    """"resourceId":""",
    """"category":"DatabaseWaitStatistics"""",
    """"operationName":"DatabaseWaitStatistcsEvent""""
  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
	  """"DatabaseName":"({db_name}[^"]+)""""
  ]


}
```