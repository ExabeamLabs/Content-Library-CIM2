#### Parser Content
```Java
{
Name = "trendmicro-ds-cef-alert-trigger-success-risk"
Vendor = "Trend Micro"
Product = "Deep Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""CEF:"""
"""|Trend Micro|Deep Security Agent|"""
"""TrendMicroDsMalwareTargetType="""
]
Fields = [
"""({host}[\w.\-]+)\s+CEF:([^\|]*\|){5}({alert_name}[^\|]+)\|({alert_severity}[^\|]+)"""
"""CEF:([^\|]*\|){4}({alert_id}\d+)"""
"""\Wdvchost=({src_host}.+?)(\s+\w+=|\s*$)"""
"""\Wcs3=({malware_url}.+?)(\s+\w+=|\s*$)"""
"""\Wact=({result}.+?)(\s+\w+=|\s*$)"""
"""({alert_type}Malware)"""
]
ParserVersion = "v1.0.0"


}
```