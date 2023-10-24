#### Parser Content
```Java
{
Name = pan-gp-csv-vpn-logout-success-succeeded
  ParserVersion = v1.0.0
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
"""globalprotect""",
"""user logout succeeded""",
"""-logout-succ"""
  ]
  Fields = [
    """({time}\d\d\d\d/\d\d/\d\d \d+:\d+:\d+)""",
    """User name:\s*({user}[\w\.\-]{1,40}\$?)""",
    """User name:\s*({email_address}[^@\s]+@[^\s,]+),""",    
    """globalprotectgateway-\S+?,({host}[\w.-]+?),""",
    """SYSTEM,({vpn_client}[^,]+),""",
    """\WReason:\s*({result_reason}[^",]+?)\.?(\s+\w+=|[",]|\s*$)""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]


}
```