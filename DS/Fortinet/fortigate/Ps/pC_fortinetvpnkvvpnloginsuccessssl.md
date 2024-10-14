#### Parser Content
```Java
{
Name = fortinet-vpn-kv-vpn-login-success-ssl
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd 'time='HH:mm:ss"
  Conditions = [ """SSL tunnel established""", """tunnel-up""", """user=""" ]

fortinet-ssl-vpn = {
  Vendor = Fortinet
  Product = FortiGate
  TimeFormat = "yyyy-MM-dd 'time='HH:mm:ssZ"
  Fields = [
    """({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d([+-]\d\d:\d\d)?)""",
    """\Wdevname="*({host}[\w\-.]+)""",
    """\Wremip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wtunnelip=(\(null\)|({src_translated_ip}[A-Fa-f:\d.]+))""",
    """\Wuser="(.+?\\\\)?(?:N\/A|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """\Wuser="(?:N\/A|({email_address}[^\s@"]+@[^\s@"]+))"""",
    """\Wmsg="({event_name}[^"]+)""",
    """\Wsentbyte=({bytes_out}\d+)""",
    """\Wrcvdbyte=({bytes_in}\d+)""",
    """\Wgroup="({realm}[^"]+)""",
    """\Wtz="?({tz}[^"]+)"""
  ]
  DupFields = [ "host->dest_host", "user->account" 
}
```