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
     """IP\s*=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """%(ASA|FTD)-({priority}\d+)-({event_code}\d+)""",
     """Group = (\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({group_name}[^,]+)),"""
   ]
 

}
```