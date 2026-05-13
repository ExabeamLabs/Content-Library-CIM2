#### Parser Content
```Java
{
Name = trendmicro-vone-cef-configuration-modify-success-systemauditlog
  Vendor = Trend Micro
  Product = Vision One
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """|Trend Micro|Trend Vision One|""", """|900004|""", """Trend Vision One System Audit Log""" ]
  Fields = [
    """rt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """CEF:([^\|]*\|){4}({event_code}[^|]+)""",
    """CEF:([^\|]*\|){5}({event_category}[^|]+)""",    
    """cat=(Unknown|({category}[^=,]+))(\s*,\S+)?\s+\w+=""",
    """({app}Trend Vision One)""",
    """\d\d:\d\d:\d\d ({host}[\w.-]+)\s""",
    """cs1=({operation}({event_name}[^=]+?))\s+\w+=""",
    """msg=\{({additional_info}[^=]+?)\}\s*(\s*$|(\s+\w+=))"""
  ]
ParserVersion = "v1.0.0"  


}
```