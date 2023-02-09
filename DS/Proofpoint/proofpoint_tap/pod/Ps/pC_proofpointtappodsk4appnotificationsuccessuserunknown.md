#### Parser Content
```Java
{
Name = proofpoint-tappod-sk4-app-notification-success-userunknown
  Vendor = Proofpoint
  Product = Proofpoint TAP/POD
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"qid"""",""""pps"""",""""cid"""","""User unknown"""" ]
  Fields = [
    """"ts"+:\s+"+({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"qid"+:\s+"+({alert_id}[^"]+)""",
    """({additional_info}User unknown)"""
  ]


}
```