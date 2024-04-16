#### Parser Content
```Java
{
Name = openvpn-ov-str-app-activity-datachannel
  Vendor = Open VPN
  Product = Open VPN
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "MMM dd HH:mm:ss"]
  Conditions = [
    """openvpn[""",
    """Data Channel"""
  ]
  Fields = [
    """({time}\w+\s+\d+ \d+:\d+:\d+)"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({host}[\w.\-]+)\s+openvpn\[({dest_port}\d+)\]""",
    """Data Channel[^:]*?:\s*({event_name}.+?)\s*$"""
  ]
  DupFields = [ "host->src_host" ]
  ParserVersion = "v1.0.0"


}
```