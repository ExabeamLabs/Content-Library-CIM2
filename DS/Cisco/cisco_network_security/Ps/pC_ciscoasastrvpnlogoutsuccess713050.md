#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-logout-success-713050
   ParserVersion = v1.0.0
   Vendor = Cisco
   Product = Cisco Network Security
   TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
   Conditions = [ """ Connection terminated for """ , """-713050""", """Reason:""", """ Remote Proxy """, """ Local Proxy """ ]
   Fields = [
     """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
     """\s(({host}[\w.\-]+))\s+([-\s:]+)?%\w+\-""",
     """({time}\w+ \d+ \d\d\d\d \d+:\d+:\d\d)""",
     """[\s\t]+\d\d:\d\d:\d\d\s+({host}[\w.\-]+).+?%\w+\-""",
     """IP\s*=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """%(ASA|FTD)-({priority}\d+)-({event_code}\d+)""",
     """Group = (\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({group_name}[^,]+)),"""
   ]
 

}
```