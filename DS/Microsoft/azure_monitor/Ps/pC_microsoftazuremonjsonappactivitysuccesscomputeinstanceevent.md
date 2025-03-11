#### Parser Content
```Java
{
Name = microsoft-azuremon-json-app-activity-success-computeinstanceevent
  Product = Azure Monitor
  ParserVersion = v1.0.0
  Conditions = [
    """"resourceId":""",
    """"category":"ComputeInstanceEvent"""",
    """"operationName":"""
  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
	  
  ]


}
```