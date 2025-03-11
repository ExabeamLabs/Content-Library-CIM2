#### Parser Content
```Java
{
Name = cisco-fp-kv-app-notification-eventdesc
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """event_desc="""", """event_subtype=""", """rec_type_desc=""" ]
  Fields = [
    """event_sec=({time}\d{10})""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """sensor=({host}[\w\-\.]+)""",
    """event_subtype=({event_subtype}\d+)""",
    """src_host=(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-.]+))""",
    """mac_address=({src_mac}[^=]+?)\s\w+=""",
    """app_proto=({app_protocol}[^\s]+)""",
    """ip_proto=({protocol}[^\s]+)""",
    """event_desc="({event_name}[^"]+)""""
  ]


}
```