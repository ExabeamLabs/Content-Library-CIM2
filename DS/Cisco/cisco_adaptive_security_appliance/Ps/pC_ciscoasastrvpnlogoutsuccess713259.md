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
     """Username = ({user}[\w\.\-\!\#\^\~]{1,40}\$?)(,|\s*$)""",
     """IP = ({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """%(FTD|ASA)(-\w+)?-({priority}\d+)-({event_code}\d+)""",
     """Group = (\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({group_name}[^,]+)),"""
   ]
 

}
```