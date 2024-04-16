#### Parser Content
```Java
{
Name = proofpoint-tappod-sk4-app-notification-success-hostnotfound
  Vendor = Proofpoint
  Product = Proofpoint Email Protection
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"qid"""",""""pps"""",""""cid"""","""DSN: Host unknown""" ]
  Fields = [
    """"ts"+:\s*"+({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"qid"+:\s*"+({alert_id}[^"]+)""",
    """({event_name}DSN: Host unknown)""",
    """\Wdproc=({event_category}.+?)\s*(\w+=|$)"""
    """({app}Proofpoint)""",
    """({additional_info}host not found)"""
    """({additional_info}DSN: Host unknown)"""
  ]


}
```