#### Parser Content
```Java
{
Name = microsoft-azuremon-json-app-activity-success-amlcomputeclusterevent
  Product = Azure Monitor
  ParserVersion = v1.0.0
  Conditions = [
    """"resourceId":""",
    """"category":"AmlComputeClusterEvent"""",
    """"operationName":"""
  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
	  
  ]


}
```