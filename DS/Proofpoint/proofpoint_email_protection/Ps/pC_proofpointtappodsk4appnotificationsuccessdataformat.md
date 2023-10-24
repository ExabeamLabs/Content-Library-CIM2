#### Parser Content
```Java
{
Name = proofpoint-tappod-sk4-app-notification-success-dataformat
  Vendor = Proofpoint
  Product = Proofpoint Email Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"qid"""",""""pps"""",""""cid"""","""DSN: Data format error""" ]
  Fields = [
    """"ts"+:\s*"+({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"qid"+:\s*"+({alert_id}[^"]+)""",
    """({additional_info}DSN: Data format error)"""
  ]
  ParserVersion = v1.0.0


}
```