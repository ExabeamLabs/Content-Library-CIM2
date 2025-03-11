#### Parser Content
```Java
{
Name = microsoft-azuremon-json-app-activity-success-synapserbacoperations
  Product = Azure Monitor
  ParserVersion = v1.0.0
  Conditions = [
    """"resourceId":""",
    """"category":"SynapseRbacOperations"""",
    """"operationName":"""
  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
    """"resultDescription":"({additional_info}[^"]+)"""
  ]


}
```