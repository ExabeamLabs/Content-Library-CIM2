#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-logout-success-713259
   ParserVersion = v1.0.0
   Vendor = Cisco
   Product = Cisco Adaptive Security Appliance
   TimeFormat = "MMM dd yyyy HH:mm:ss"
   Conditions = [ """Session is being torn down""", """-713259""" ]
   Fields = [
     """[\s\t]+\d\d:\d\d:\d\d\s+({host}[\w.\-]+).+?%ASA""",
     """({time}\w+ \d+ \d\d\d\d \d+:\d+:\d+)""",
     """Username = ({user}[^,@]+?)(,|\s*$)""",
     """IP = ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
     """%ASA-({priority}\d+)-({event_code}\d+)""",
     """Group = (\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({group_name}[^,]+)),"""
   ]
 

}
```