#### Parser Content
```Java
{
Name = f5-apm-str-vpn-success-allow
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 Access Policy Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
"""<ACCESS_POLICY_COMPLETED>"""
"""Policy Result: allow"""
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[^\s]+)\s+({host}[^\s]+)\s+[^\s]+\s+Rule.+?Session ID:\s+({session_id}[^\|]+)\|ClientIP:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Username:({user}[^\s][^\|]*?)\|""",
    """Username:\s({user}[^\s][^\|]*?)\|""",
    """Username: n/a.+emailAddress=[^,]+,CN=({user}[^,]+)""",
    """User Agent:({user_agent}[^|]+)"""	
  ]


}
```