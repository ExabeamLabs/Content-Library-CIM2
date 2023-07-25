#### Parser Content
```Java
{
Name = proofpoint-tappod-sk4-app-notification-success-localconfiguration
  Vendor = Proofpoint
  Product = Proofpoint Email Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"qid"""",""""pps"""",""""cid"""","""DSN: Local configuration error""" ]
  Fields = [
    """"ts"+:\s*"+({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"qid"+:\s*"+({alert_id}[^"]+)""",
    """({additional_info}DSN: Local configuration error)"""
  ]
  ParserVersion = v1.0.0


}
```