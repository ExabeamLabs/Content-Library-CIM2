#### Parser Content
```Java
{
Name = "cisco-asa-str-app-notification-tcptranslation"
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """%ASA-6-305011:""", """ Built dynamic TCP translation """ ]
  Fields = [
    """:\s*%ASA-6-({event_code}\d+)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s\S+\s+:\s+%ASA-6-305011:""",
    """({time}\w{3} (\d\d| \d) \d\d\d\d (\d\d| \d):\d\d:\d\d)""",
    """\w{3}\s+\d+\s+\d+:\d+:\d+\s+({host}(\d{1,3}\.){3}\d{1,3})"""
    """(2\d\d\d|({host}[\w+\.-]+))\s+(\S*:\s*)?%ASA-\d+-\d+:""",
    """\s*({event_name}Built dynamic TCP translation)""",
    """(?i)(LAN|inside):({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({src_port}\d+)""",
    """(?i)(INET|Bank):({src_translated_ip}(\d{1,3}\.){3}\d{1,3})\/({src_translated_port}\d+)""",
    """:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({src_port}\d+) to (outside|externaprod):({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({dest_port}\d+)"""
    """from OUTSIDE:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({src_port}\d+).*?to OUTSIDE:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({dest_port}\d+)"""
  ]


}
```