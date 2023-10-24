#### Parser Content
```Java
{
Name = "microsoft-365defender-json-alert-trigger-success-publish-1"
  Vendor = Microsoft
  Product = Microsoft Defender for Endpoint
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"category":"AdvancedHunting-AlertInfo"""", """"operationName":"Publish"""", """"Severity":""", """"Title":""" ]
  Fields = [
    """"Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"hostname":"({host}[^"]+)"""",
    """"AlertId":"({alert_id}[^"]+)"""",
    """"Title":"({alert_name}[^"]+)"""",
    """"(C|c)ategory":"({alert_type}[^"]+)"""",
    """"Severity":"({alert_severity}[^"]+)"""",
    """"DetectionSource":"({alert_source}[^"]+)""""
  ]
  DupFields = [ "alert_name->alert_subject" ]
  ParserVersion = "v1.0.0"


}
```