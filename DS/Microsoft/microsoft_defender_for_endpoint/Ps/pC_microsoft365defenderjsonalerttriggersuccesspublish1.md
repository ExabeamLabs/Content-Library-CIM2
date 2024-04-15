#### Parser Content
```Java
{
Name = "microsoft-365defender-json-alert-trigger-success-publish-1"
  Vendor = Microsoft
  Product = Microsoft Defender for Endpoint
  TimeFormat = "yyyy-MM-dd'T'HH:mm:SS"
  Conditions = [ """"category":"AdvancedHunting-AlertInfo"""", """"operationName":"Publish"""", """"Severity":""", """"Title":""" ]
  Fields = [
    """"Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"hostname":"({host}[^"]+)"""",
    """"AlertId":"({alert_id}[^"]+)"""",
    """"Title":"({alert_name}[^"]+)"""",
    """"Category":"({alert_type}[^"]+)"""",
    """"Severity":"({alert_severity}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```