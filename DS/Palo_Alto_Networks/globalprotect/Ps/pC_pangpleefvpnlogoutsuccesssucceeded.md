#### Parser Content
```Java
{
Name = pan-gp-leef-vpn-logout-success-succeeded
  ParserVersion = v1.0.0
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy/MM/dd HH:mm:ss"]
  Conditions = [
"""LEEF:""",
"""globalprotect""",
"""user logout succeeded""",
"""-logout-succ"""
  ]
  Fields = [
    """({time}\d\d\d\d/\d\d/\d\d \d+:\d+:\d+)""",
    """User name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """User name:\s*({email_address}[^@\s]+@[^\s,]+),""",
    """DeviceName =({host}[\w\-.]+)""",
    """\WReason:\s*({result_reason}[^",]+?)\.?(\s+\w+=|[",]|\s*$)""",
    """:\d\d:\d\d (-|({host}[\w.-]+))\s""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
    """DeviceName =({device_name}({host}[\w\-.]+))""",
    """SerialNumber=({serial_num}[^\|]+)"""
  ]


}
```