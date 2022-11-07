#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-logout-success-713050
   ParserVersion = v1.0.0
   Vendor = Cisco
   Product = Cisco Adaptive Security Appliance
   TimeFormat = "MMM dd yyyy HH:mm:ss"
   Conditions = [ """ Connection terminated for """ , """-713050""" ]
   Fields = [
     """({time}\w+ \d+ \d\d\d\d \d+:\d+:\d\d)""",
     """[\s\t]+\d\d:\d\d:\d\d\s+({host}[\w.\-]+).+?%ASA""",
     """IP\s*=\s*({src_ip}[A-Fa-f:\d.]+)""",
     """%(ASA|FTD)-({priority}\d+)-({event_code}\d+)""",
     """Group = (\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({group_name}[^,]+)),"""
   ]
 

}
```