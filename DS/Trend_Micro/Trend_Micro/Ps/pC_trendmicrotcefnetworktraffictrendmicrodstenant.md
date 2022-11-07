#### Parser Content
```Java
{
Name = trendmicro-t-cef-network-traffic-trendmicrodstenant
  ParserVersion = v1.0.0
  Vendor = Trend Micro
  Product = Trend Micro
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""TrendMicroDsTenant""",
"""TrendMicroDsFrameType=IP"""
  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """[\|\s]dvchost=({host}[^\|\s"]+)""",
    """[\|\s]dst=({dest_ip}[a-fA-F\d.:]+)""",
    """[\|\s]dpt=({dest_port}\d+)""",
    """[\|\s]src=({src_ip}[a-fA-F\d.:]+)""",
    """[\|\s]spt=({src_port}\d+)""",
    """[\|\s]proto=({protocol}[^\|\s]+?)[\s\|]""",
    """[\|\s]smac=({src_mac}[^\|\s]+)""",
    """[\|\s]in=({bytes}\d+)""",
    """[\|\s]act=({operation}[^\|\s]+)""",
    """[\|\s]dmac=({dest_mac}[^\s\|]+?)[\s\|]""",
    """CEF:(\s*\d+)\|(([^\|]+)\|){4}({alert_name}[^\|]+)""",
  ]


}
```