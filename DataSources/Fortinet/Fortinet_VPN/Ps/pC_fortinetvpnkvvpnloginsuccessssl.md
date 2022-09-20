#### Parser Content
```Java
{
Name = fortinet-vpn-kv-vpn-login-success-ssl
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd 'time='HH:mm:ss"
  Conditions = [ """SSL tunnel established""", """tunnel-up""", """user=""" ]

fortinet-ssl-vpn = {
  Vendor = Fortinet
  Product = Fortinet VPN
  TimeFormat = "yyyy-MM-dd 'time='HH:mm:ssZ" 
  Fields = [
    """({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d([+-]\d\d:\d\d)?)""",
    """\Wdevname="*({host}[\w\-.]+)""",
    """\Wremip=({src_ip}[A-Fa-f:\d.]+)""",
    """\Wtunnelip=(\(null\)|({src_translated_ip}[A-Fa-f:\d.]+))""",
    """\Wuser="(.+?\\\\)?(?:N\/A|({user}[^\s@"]+))"""",
    """\Wuser="(?:N\/A|({email_address}[^\s@"]+@[^\s@"]+))"""",
    """\Wmsg="({event_name}[^"]+)""",
    """\Wsentbyte=({bytes_out}\d+)""",
    """\Wrcvdbyte=({bytes_in}\d+)""",
    """\Wgroup="({realm}[^"]+)"""
  ]
  DupFields = [ "host->dest_host", "user->account" 
}
```