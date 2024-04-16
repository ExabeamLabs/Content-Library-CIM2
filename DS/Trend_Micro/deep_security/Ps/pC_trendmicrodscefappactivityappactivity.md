#### Parser Content
```Java
{
Name = trendmicro-ds-cef-app-activity-appactivity
  ParserVersion = v1.0.0
  Vendor = Trend Micro
  Product = Deep Security
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","MMM dd HH:mm:ss"]
  Conditions = [ """CEF:""", """|Trend Micro|""", """|Deep Security""", """TrendMicroDsTenant=""", """TrendMicroDsTenantId=""" ]
  Fields = [
    """({time}\w+\s\d+\s\d+:\d+:\d+)\s({host}[\w\-.]+)"""
    """({host}[\w\-.]+) CEF:([^\|]*\|){5}({event_name}[^\|]+)\|""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wtarget=({dest_host}[\w\-.]+)""",
    """\Wproto=({protocol}[^=]+?)\s+(\w+=|$)""",
    """\Wspt=({src_port}\d+)""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wsmac=({src_mac}[^=]+?)\s+(\w+=|$)""",
    """\Wdmac=({dest_mac}[^=]+?)\s+(\w+=|$)""",
    """msg=({additional_info}[^=]+?)\s*\w+=""",
    """target=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
    """\scs1=({additional_info}[^=]+?)\s*\w+=""",
    """Application:\s+AUDIT_({result}[^(]+)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
    """Login succeeded for user\s+'(({domain}[^\\]+)\\\\)?(SYSTEM|({user}[\w\.\-]{1,40}\$?))""",
  ]


}
```