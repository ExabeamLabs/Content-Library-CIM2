#### Parser Content
```Java
{
Name = barracuda-waf-str-app-notification-foundcdpdu
  ParserVersion = v1.0.0
  Vendor = Barracuda
  Product = Barracuda WAF
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """] Found CDPDU""", """, bytesLeft """ ]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d+Z)"""
    """({event_name})Found CDPDU"""
    """({additional_info}Found .*)""",
  ]


}
```