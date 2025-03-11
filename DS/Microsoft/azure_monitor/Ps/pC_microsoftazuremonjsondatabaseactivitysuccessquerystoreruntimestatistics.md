#### Parser Content
```Java
{
Name = microsoft-azuremon-json-database-activity-success-querystoreruntimestatistics
  Product = Azure Monitor
  ParserVersion = v1.0.0
  Conditions = [
    """"resourceId":""",
    """"category":"QueryStoreRuntimeStatistics"""",
    """"operationName":"QueryStoreRuntimeStatisticsEvent""""
  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
	  """"DatabaseName":"({db_name}[^"]+)""""
  ]


}
```