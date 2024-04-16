#### Parser Content
```Java
{
Name = cisco-ac-str-vpn-logout-success-resume
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = AnyConnect
  TimeFormat = ["MMM dd yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssZ","MMM dd HH:mm:ss"]
  Conditions = [ """AnyConnect session lost connection. Waiting to resume.""" ]
  Fields = [
    """\w{1,3}\s{1,2}\d{1,2}\s\d\d:\d\d:\d\d\s({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({src_host}[\w.\-]+))\s%ASA-""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD-""",
    """({time}\w+ \d+ \d+:\d+:\d+)"""
    """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
    """({time}\w+ \d+ \d\d\d\d \d+:\d+:\d+)""",
    """User\s+<(({email_address}[^@>]+@[^>]+)|(({domain}[^\\>]+)\\+)?({user}[\w\.\-]{1,40}\$?))>""",    
    """User\s<({full_name}[^,@]+\s\w+)>""",
    """IP\s<({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """User\s+<({email_address}[^@>]+@[^@>]+)>""",
    """\sGroup\s*<({group_name}[^>]+)>"""
    """\sUser\s*<({user}[\w\.\-]{1,40}\$?)>"""
  ]


}
```