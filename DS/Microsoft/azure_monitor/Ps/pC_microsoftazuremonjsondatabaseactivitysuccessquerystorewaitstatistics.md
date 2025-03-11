#### Parser Content
```Java
{
Name = microsoft-azuremon-json-database-activity-success-querystorewaitstatistics
  Product = Azure Monitor
  ParserVersion = v1.0.0
  Conditions = [
    """"resourceId":""",
    """"category":"QueryStoreWaitStatistics"""",
    """"operationName":"QueryStoreWaitStatisticsEvent""""
  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
	  """"DatabaseName":"({db_name}[^"]+)""""
  ]


}
```