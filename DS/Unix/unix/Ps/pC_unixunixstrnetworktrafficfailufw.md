#### Parser Content
```Java
{
Name = unix-unix-str-network-traffic-fail-ufw
  Vendor = Unix
  Product = Unix
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """UFW""", """IN=""", """DST=""", """LEN=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s+({event_category}[^:]+):\s+""",
    """IN=({src_interface}[^=]+?)\s+\w+=""",
    """OUT=({dest_interface}[^=]+?)\s+\w+=""",
    """MAC=({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})""",
    """SPT=({src_port}\d{1,5})""",
    """DPT=({dest_port}\d{1,5})""",
    """SRC=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d).?\b){4}))(:({src_port}\d+))?\s""",
    """DST=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d).?\b){4}))(:({dest_port}\d+))?\s""",
    """LEN=({bytes}\d+)""",
    """PROTO=({protocol}\d+)""",
    """\[UFW ({action}[^\]]+)\]"""
  ]


}
```