#### Parser Content
```Java
{
Name = openvpn-ov-kv-app-notification-openvpn
  Vendor = Open VPN
  Product = Open VPN
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "MMM dd HH:mm:ss"]
  Conditions = [ """openvpn[""", """Authenticate/Decrypt packet error:""" ]
  Fields = [
    """({time}\w+\s+\d+ \d+:\d+:\d+)"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({host}[\w.\-]+)\s+openvpn\[({dest_port}\d+)\]""",
    """Authenticate/Decrypt packet error:\s*({failure_reason}[^:]+?):""",
    """\[\s*\#({process_id}\d+)\s*\]""",
  ]
  DupFields = [ "host->src_host" ]


}
```