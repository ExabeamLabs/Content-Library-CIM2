#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-appactivity
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "epoch"
  Conditions = [ """destinationServiceName =Office 365""", """"activityType":""", """"activity":""", """"activityResultStatus":""" ]
  Fields = [
    """\Wcat=({category}[^\s]+)""",
    """destinationServiceName =({app}.+?)\s+(\w+=|$)""",
    """\WflexString1=({operation}.+?)\s+(\w+=|$)""",
    """"activity":"({event_name}[^"]+)"""",
    """\WsourceServiceName =({resource}.+?)\s+(\w+=|$)""",
    """"activityResultStatus":"({result}[^"]+)"""",
    """"targetResourceType":"({object_type}[^"]+)"""",
    """"userPrincipalName":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"targets":\[\{.*?"objectId":"({object_id}[^"]+)"""",
    """"activityDateInMillis":({time}\d{13})""",
    """"targets":\[\{.*?"@odata.type":"({additional_info}[^"]+)"""",
    """\Wfname=({file_name}.+?)\s+(\w+=|$)""",
    """\Wmsg=(({description}[^=]+ updated).*?|({=description}.+?))\s+(\w+=|$)""",
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```