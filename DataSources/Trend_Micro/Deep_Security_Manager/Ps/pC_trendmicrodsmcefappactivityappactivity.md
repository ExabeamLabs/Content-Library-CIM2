#### Parser Content
```Java
{
Name = trendmicro-dsm-cef-app-activity-appactivity
  ParserVersion = v1.0.0
  Vendor = Trend Micro
  Product = Deep Security Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""", """|Trend Micro|""", """|Deep Security""", """TrendMicroDsTenant=""", """TrendMicroDsTenantId=""" ]
  Fields = [
    """({host}[\w\-.]+) CEF:([^\|]*\|){5}({event_name}[^\|]+)\|""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\Wdst=({dest_ip}[A-Fa-f:\d.]+)""",
    """\Wtarget=({dest_host}[\w\-.]+)""",
    """\Wproto=({protocol}[^=]+?)\s+(\w+=|$)""",
    """\Wspt=({src_port}\d+)""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wsmac=({src_mac}[^=]+?)\s+(\w+=|$)""",
    """\Wdmac=({dest_mac}[^=]+?)\s+(\w+=|$)""",
    """msg=({additional_info}[^=]+?)\s*\w+=""",
    """target=(({src_ip}[A-Fa-f:\d.]+)|({src_host}[^\s]+))\s""",
    """\scs1=({additional_info}[^=]+?)\s*\w+=""",
    """Application:\s+AUDIT_({result}[^(]+)""",
    """Login succeeded for user\s+'(({domain}[^\\]+)\\\\)?(SYSTEM|({user}[^']+))""",
  ]


}
```