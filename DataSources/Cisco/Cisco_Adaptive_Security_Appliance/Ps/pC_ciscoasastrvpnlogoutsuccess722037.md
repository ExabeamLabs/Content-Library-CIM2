#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-logout-success-722037
   ParserVersion = v1.0.0
   Vendor = Cisco
   Product = Cisco Adaptive Security Appliance
   TimeFormat = "MMM dd yyyy HH:mm:ss"
   Conditions = [ """SVC closing connection:""", """-722037""" ]
   Fields = [
     """({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)""",
     """[\s\t]+\d\d:\d\d:\d\d\s+({host}[\w.\-]+).+?%ASA""",
     """({host}[^\s]+)\s+:\s+%FTD-""",
     """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
     """%(ASA|FTD)-({priority}\d+)-({event_code}\d+)""",
     """Group\s*<({group_name}.*?)>""",
     """IP\s*<({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})>\s*({event_name}.*?):\s""",
     """User\s*<({user}[^@>]+)(?:@({email_domain}[^>]+))?>"""
   ]
 

}
```