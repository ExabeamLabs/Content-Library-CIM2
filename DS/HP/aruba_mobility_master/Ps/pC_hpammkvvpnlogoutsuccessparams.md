#### Parser Content
```Java
{
Name = hp-amm-kv-vpn-logout-success-params
  Vendor = HP
  Product = Aruba Mobility Master
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """params:""", """mgmtd[""", """alarm_type="""]
  Fields = [
    """(\w{1,3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+))""",
    """params:({additional_info}[^:]+?)\s*$""",
    """src=({src_ip}[a-fA-F\d:\.]+)""",
    """dst=({dest_ip}[a-fA-F\d:\.]+)""",
    """mgmtd([^\s]+\s){2}({event_name}[^:]+?)\sparams:""",
  ]


}
```