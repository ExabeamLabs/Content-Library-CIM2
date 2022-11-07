#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-logout-success-716002
   ParserVersion = v1.0.0
   Vendor = Cisco
   Product = Cisco Adaptive Security Appliance
   TimeFormat = "MMM dd yyyy HH:mm:ss"
   Conditions = [ """WebVPN session terminated""" , """-716002""" ]
   Fields = [
     """({time}\w+ \d+ \d\d\d\d \d+:\d+:\d\d)""",
     """[\s\t]+\d\d:\d\d:\d\d\s+({host}[\w.\-]+).+?%ASA""",
     """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
     """({host}[^\s]+)\s+:\s+%FTD-""",
     """({host}[^\s]+)\s+:\s+%ASA-""",
     """User\s+<({user}[^>]+)>""",
     """IP\s+<({src_ip}[^>]+)>""",
     """%(ASA|FTD)-({priority}\d+)-({event_code}\d+)""",
     """Group\s*<({group_name}.*?)>"""
   ]
   DupFields = [ "group_name->realm" ]
 

}
```