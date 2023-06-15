#### Parser Content
```Java
{
Name = hp-3parstoreserv-str-app-activity-cli
  ParserVersion = "v1.0.0"
  Vendor = HP
  Product = HPE 3PAR StoreServ
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ cli_command """, """ sw_cli """, """3PAR""" ]
  Fields = [
    """\s({host}[\w-]+)\s+cli_command""",
    """({event_name}cli_command)""",
    """sw_cli\s\{({user}[^\s]+)\s({privileges}[^\s]+)[^.:]+?\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)\s\d+\}""",
    """\d+\}\s+\{({process_command_line}[^"]+?)\s*\}\s\{"""
  ]


}
```