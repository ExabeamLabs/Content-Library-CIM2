#### Parser Content
```Java
{
Name = cisco-fp-str-vpn-logout-success-722037
   ParserVersion = v1.0.0
   Vendor = Cisco
   Product = Cisco Network Security
   TimeFormat = ["MMM dd yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss"]
   Conditions = [ """SVC closing connection:""", """-722037""", """%FTD""" ]
   Fields = [
     """({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)""",
     """[\s\t]+\d\d:\d\d:\d\d\s+({host}[\w.\-]+).+?%ASA""",
     """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD-""",
     """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
     """%(FTD|ASA)(-\w+)?-({priority}\d+)-({event_code}\d+)""",
     """Group\s*<({group_name}.*?)>""",
     """IP\s*<({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))>\s*({event_name}.*?):\s""",
     """User\s*<(({domain}[^\\\/]+)[\\\/])?(({email_address}[^@>]+@[^>\.]+\.[^>]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*>"""
   ]
 

}
```