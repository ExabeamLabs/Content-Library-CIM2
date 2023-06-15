#### Parser Content
```Java
{
Name = trendmicro-ds-cef-network-traffic-trendmicrodstenant
  ParserVersion = v1.0.0
  Vendor = Trend Micro
  Product = Deep Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""TrendMicroDsTenant""",
"""TrendMicroDsFrameType=IP"""
  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """[\|\s]dvchost=({host}[^\|\s"]+)""",
    """[\|\s]dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """[\|\s]dpt=({dest_port}\d+)""",
    """[\|\s]src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """[\|\s]spt=({src_port}\d+)""",
    """[\|\s]proto=({protocol}[^\|\s]+?)[\s\|]""",
    """[\|\s]smac=({src_mac}[^\|\s]+)""",
    """[\|\s]in=({bytes}\d+)""",
    """[\|\s]act=({operation}[^\|\s]+)""",
    """[\|\s]dmac=({dest_mac}[^\s\|]+?)[\s\|]""",
    """CEF:(\s*\d+)\|(([^\|]+)\|){4}({alert_name}[^\|]+)""",
    """cat=({category}[^=]+?)\s*\w+=""",
    """name=({alert_name}[^=]+?)\s*\w+=""",
    """sev=({alert_severity}[^\s]+)"""
  ]


}
```