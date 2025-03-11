#### Parser Content
```Java
{
Name = microsoft-azuremon-json-app-activity-success-querysearch
  Product = Azure Monitor
  ParserVersion = v1.0.0
  Conditions = [
    """"resourceId":""",
    """"category":"OperationLogs"""",
    """"operationName":"Query.Search""""
  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
    """"Query":"({query}[^"]+)""""
    """"durationMS":({duration}\d+)"""
  ]


}
```