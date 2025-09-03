#### Parser Content
```Java
{
Name = fortinet-firewall-str-network-close-success-teardown
  Vendor = Fortinet
  Product = Fortinet Enterprise Firewall
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """ Teardown dynamic """, """translation from """, """ duration """ ]
  Fields = [
    """({time}\w{3}\s+\d{1,2}\s+\d\d:\d\d:\d\d)\s""",
    """\s({host}[\w\-.]+)\sTeardown dynamic""",
    """({action}Teardown) dynamic ({protocol}[^\s]+) translation""",
    """from\s({src_interface}[^:]+):({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\/({src_port}\d+))?\sto\s({dest_interface}[^:]+):({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\/({dest_port}\d+))?\s""",
    """\sduration\s({connection_duration}[^\s]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```