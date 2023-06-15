#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-json-app-activity-appactivity
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Azure AD Activity Logs
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
    """"activityDateInMillis":({time}\d{13})""",
    """"targets":\[\{.*?"@odata.type":"({additional_info}[^"]+)"""",
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  DupFields = ["operation->event_name", "category->resource"]


}
```