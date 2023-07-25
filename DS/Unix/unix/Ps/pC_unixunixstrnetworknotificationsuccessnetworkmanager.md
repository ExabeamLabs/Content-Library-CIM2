#### Parser Content
```Java
{
Name = unix-unix-str-network-notification-success-networkmanager
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """NetworkManager[""", """]: """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s+({event_category}[^:]+):\s+""",
    """\]:\s*({additional_info}[^$]+?)\s*$"""
  ]
  ParserVersion = v1.0.0


}
```