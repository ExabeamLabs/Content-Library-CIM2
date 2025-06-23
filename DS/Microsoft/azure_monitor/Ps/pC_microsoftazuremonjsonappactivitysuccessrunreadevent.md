#### Parser Content
```Java
{
Name = microsoft-azuremon-json-app-activity-success-runreadevent
  Product = Azure Monitor
  ParserVersion = v1.0.0
  Conditions = [
    """"resourceId":""",
    """"category":"RunReadEvent"""",
    """"operationName":"""
  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
    """"CorrelationId":"({correlation_id}[^"]+)"""
    """"Identity":"\{\\*"UserName\\":\\*"({full_name}[^"\\]+)"""
    """"Identity":"\{[^\}]+\\*"UserObjectId\\":\\*"({object}[^"\\]+)""""
  ]


}
```