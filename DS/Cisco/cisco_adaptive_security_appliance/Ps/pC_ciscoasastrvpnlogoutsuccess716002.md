#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-logout-success-716002
   ParserVersion = v1.0.0
   Vendor = Cisco
   Product = Cisco Adaptive Security Appliance
   TimeFormat = ["MMM dd yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssZ"]
   Conditions = [ """WebVPN session terminated""" , """-716002""" ]
   Fields = [
     """({time}\w+ \d+ \d\d\d\d \d+:\d+:\d\d)""",
     """\w{1,3}\s{1,2}\d{1,2}\s(\d{4})?\s\d\d:\d\d:\d\d\s({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w.\-]+))\s.+?ASA-""",
     """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
     """({host}[^\s]+)\s+:\s+%FTD-""",
     """({host}[^\s]+)\s+:\s+%ASA-""",
     """User\s*<(({domain}[^\\\/]+)[\\\/])?(({email_address}[^@>]+@[^>\.]+\.[^>]+)|({user}[\w\.\-]{1,40}\$?))\s*>""",
     """IP\s+<({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?>""",
     """%(FTD|ASA)(-\w+)?-({priority}\d+)-({event_code}\d+)""",
     """Group\s*<({group_name}.*?)>"""
    """\sUser\s*<({user}[\w\.\-]{1,40}\$?)>"""
   ]
   DupFields = [ "group_name->realm" ]
 

}
```