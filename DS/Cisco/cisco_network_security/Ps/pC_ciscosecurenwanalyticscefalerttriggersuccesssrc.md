#### Parser Content
```Java
{
Name = cisco-securenwanalytics-cef-alert-trigger-success-src
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = "v1.0.0"
  TimeFormat =  "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """CEF:""", """Cisco|Stealthwatch""", """src""", """externalId""", """dvchost""" ]
  Fields = [
    """dvchost=({host}[^\s]+)""",
    """start=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst=(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """msg=({additional_info}[^=]+)\s+""",
    """externalId=({alert_id}[^\s]+)""",
    """dvc=({host_ip}[a-fA-F0-9.:]+)""",
    """CEF:([^\|]+\|){4}({event_code}[^\|]+)""",
    """CEF:([^\|]+\|){6}({alert_severity}[^\|]+)""",
    """CEF:([^\|]+\|){5}({alert_name}[^\|]+)""",
    """CEF:([^\|]+\|){5}({alert_type}[^\|]+)""",
    """CEF:([^\|]+\|){5}({event_name}[^\|]+)""",
  ]


}
```