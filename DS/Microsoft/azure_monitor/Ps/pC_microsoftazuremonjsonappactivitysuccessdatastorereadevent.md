#### Parser Content
```Java
{
Name = microsoft-azuremon-json-app-activity-success-datastorereadevent
  Product = Azure Monitor
  ParserVersion = v1.0.0
  Conditions = [
    """"resourceId":""",
    """"category":"DataStoreReadEvent"""",
    """"operationName":"""
  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
	  
  ]


}
```