#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-appactivity
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Office 365
  TimeFormat = "epoch"
  Conditions = [ """destinationServiceName =Office 365""", """"activityType":""", """"activity":""", """"activityResultStatus":""" ]
  Fields = [
    """\Wcat=({category}[^\s]+)""",
    """\WdestinationServiceName =({app}.+?)\s+(\w+=|$)""",
    """\WflexString1=({operation}.+?)\s+(\w+=|$)""",
    """"activity":"({event_name}[^"]+)"""",
    """\WsourceServiceName =({resource}.+?)\s+(\w+=|$)""",
    """"activityResultStatus":"({result}[^"]+)"""",
    """"targetResourceType":"({object_type}[^"]+)"""",
    """"userPrincipalName":"(({email_address}[^@"]+?@[^"]+)|({user}[^"]+))"""",
    """"targets":\[\{.*?"objectId":"({object_id}[^"]+)"""",
    """"activityDateInMillis":({time}\d+)""",
    """"targets":\[\{.*?"@odata.type":"({additional_info}[^"]+)"""",
    """\Wfname=({file_name}.+?)\s+(\w+=|$)""",
    """\Wmsg=(({description}[^=]+ updated).*?|({=description}.+?))\s+(\w+=|$)""",
    """"ipAddress":"({src_ip}[a-fA-F:\d.]+)"""
  ]


}
```