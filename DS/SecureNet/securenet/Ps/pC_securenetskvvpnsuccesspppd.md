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
    """\Wusername="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """\Wsrcip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """\Wvirtual_ip="({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""""
  ]
  DupFields = ["user->account"]
  ParserVersion = "v1.0.0"


}
```