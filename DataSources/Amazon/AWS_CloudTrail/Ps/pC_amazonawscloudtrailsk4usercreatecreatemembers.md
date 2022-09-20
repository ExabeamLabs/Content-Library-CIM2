#### Parser Content
```Java
{
Name = amazon-awscloudtrail-sk4-user-create-createmembers
  ParserVersion = v1.0.0
  Vendor = Amazon
  Product = AWS CloudTrail
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"source":"aws.guardduty"""", """"eventName":"CreateMembers"""" ]
  Fields = [
    """"eventTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"sourceIPAddress":"({src_ip}[A-Fa-f:\d.]+)""",
    """suser=(?:(?i)anonymous|({user}[^=]+?))\s+\w+=""",
    """"userIdentity":[^=]+?userName":"({user}[^"]+)""",
    """({event_name}CreateMembers)""",
    """"userAgent":"({user_agent}[^"]+)""",
    """"eventType":"({alert_type}[^"]+)""",
    """"eventID":"({alert_id}[^"]+)""",
    """({alert_name}CreateMembers)""",
    """"result":"[^"]*({action}rejected)""",
    """CreateMembers[^=]+?result":"({additional_info}[^"]+)""",
    """CreateMembers[^=]+?accountId":"({account_id}\d+)"""
  ]


}
```