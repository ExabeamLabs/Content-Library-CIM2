#### Parser Content
```Java
{
Name = cisco-ac-str-vpn-logout-success-resume
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = AnyConnect
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """AnyConnect session lost connection. Waiting to resume.""" ]
  Fields = [
    """({host}[^\s]+)\s+:\s+%FTD-""",
    """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
    """({time}\w+ \d+ (\d\d\d\d )?\d+:\d+:\d+)""",
    """User\s+<(({email_address}[^@>]+@[^>]+)|(({domain}[^\\>]+)\\+)?({user}[^>]+))>""",    
    """User\s<({full_name}[^,@]+\s\w+)>""",
    """IP\s<({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """User\s+<({email_address}[^@>]+@[^@>]+)>"""
  ]


}
```