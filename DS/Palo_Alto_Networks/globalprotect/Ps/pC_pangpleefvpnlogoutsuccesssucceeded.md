#### Parser Content
```Java
{
Name = pan-gp-leef-vpn-logout-success-succeeded
  ParserVersion = v1.0.0
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [
"""LEEF:""",
"""globalprotect""",
"""user logout succeeded""",
"""-logout-succ"""
  ]
  Fields = [
    """({time}\d\d\d\d/\d\d/\d\d \d+:\d+:\d+)""",
    """User name:\s*({user}[\w.'\-\\$]+)""",
    """User name:\s*({email_address}[^@\s]+@[^\s,]+),""",
    """DeviceName =({host}[\w\-.]+)""",
    """\WReason:\s*({reason}[^",]+?)\.?(\s+\w+=|[",]|\s*$)""",
    """:\d\d:\d\d (-|({host}[\w.-]+))\s"""
  ]


}
```