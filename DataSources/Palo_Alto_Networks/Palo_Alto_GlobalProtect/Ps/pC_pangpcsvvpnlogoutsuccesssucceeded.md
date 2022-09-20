#### Parser Content
```Java
{
Name = pan-gp-csv-vpn-logout-success-succeeded
  ParserVersion = v1.0.0
  Vendor = Palo Alto Networks
  Product = Palo Alto GlobalProtect
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [
"""globalprotect""",
"""user logout succeeded""",
"""-logout-succ"""
  ]
  Fields = [
    """({time}\d\d\d\d/\d\d/\d\d \d+:\d+:\d+)""",
    """User name:\s*({user}[\w.'\-\\$]+)""",
    """User name:\s*({email_address}[^@\s]+@[^\s,]+),""",    
    """globalprotectgateway-\S+?,({host}[\w.-]+?),""",
    """SYSTEM,({vpn_client}[^,]+),""",
    """\WReason:\s*({reason}[^",]+?)\.?(\s+\w+=|[",]|\s*$)"""
  ]


}
```