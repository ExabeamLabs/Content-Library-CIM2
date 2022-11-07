#### Parser Content
```Java
{
Name = securenet-s-kv-vpn-success-pppd
  Vendor = SecureNet
  Product = SecureNet
  TimeFormat = "yyyy:MM:dd-HH:mm:ss"
  Conditions = [ """pppd-l2tp[""", """sub="vpn"""", """username=""""  ]
  Fields = [
    """({time}\d\d\d\d:\d\d:\d\d\-\d\d:\d\d:\d\d)\s+({host}[^\s]+)""",
    """\Wid="({event_code}\d+)""",
    """\Wevent="({event_name}[^"]+)"""",
    """\Wusername="({user}[^"]+)"""",
    """\Wsrcip="({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""",
    """\Wvirtual_ip="({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""""
  ]
  DupFields = ["user->account"]
  ParserVersion = "v1.0.0"


}
```