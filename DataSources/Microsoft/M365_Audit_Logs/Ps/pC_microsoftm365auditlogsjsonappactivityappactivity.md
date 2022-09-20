#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-json-app-activity-appactivity
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = M365 Audit Logs
  TimeFormat = "epoch"
  Conditions = [ """"activityResultDescription":"""",  """"activityOperationType":""", """"activityResultStatus":""" ]
  Fields = [
    """"category":"({category}[^"]+)"""",
    """({app}Office 365)""",
    """"activity":"({operation}[^"]+)"""",
    """"activityResultStatus":"({result}[^"]+)"""",
    """"activityType":"({object_type}[^"]+)"""",
    """"userPrincipalName":"(({email_address}[^@"]+?@[^"]+)|({user}[^"]+))"""",
    """"targets":\[\{.*?"objectId":"({object_id}[^"]+)"""",
    """"activityDateInMillis":({time}\d+)""",
    """"targets":\[\{.*?"@odata.type":"({additional_info}[^"]+)"""",
    """"ipAddress":"({src_ip}[a-fA-F:\d.]+)"""
  ]
  DupFields = ["operation->event_name", "category->resource"]


}
```