#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-app-activity-clientrequest
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """requestClientApplication=Azure""", """"category": "ApplicationGatewayPerformanceLog"""" ]
  Fields = [
    """"time": "({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"operationName": "({operation}[^"]+)"""",
    """"resourceId": "({object}[^"]+)""""

  ]
  ParserVersion = "v1.0.0"


}
```