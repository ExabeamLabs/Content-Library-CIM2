#### Parser Content
```Java
{
Name = fortinet-vpn-cef-vpn-logout-success-down
  ParserVersion = v1.0.0
  Vendor = Fortinet
  Product = FortiGate
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","yyyy-MM-dd 'time='HH:mm:ssz","yyyy-MM-dd 'time='HH:mm:ss"]
  Conditions = [ 
"""action="tunnel-down""""
"""subtype="vpn""""
]
  Fields = [
    """({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d([+-]\d\d:\d\d)?)""",
    """\Wdevname="+({host}[\w\-.]+)""",
    """\Wremip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wtunnelip=(\(null\)|({src_translated_ip}[A-Fa-f:\d.]+))""",
    """\Wuser="(.+?\\\\)?(?:N\/A|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """\Wuser="N\/A|({email_address}[^\s@"]+@[^\s@"]+)"""",
    """\Wmsg="({event_name}[^"]+?)\s+(\d+|")""",
    """\Wsentbyte=({bytes_out}\d+)""",
    """\Wrcvdbyte=({bytes_in}\d+)""",
    """\Wgroup="+({realm}[^"]+)""",
    """\Wtz="?({tz}[+-]\d+)"""
    """\sduration=({session_duration}[^\s]+)""",
    """\sreason="({result_reason}[^"]+)"\sduration""",
    """\saction="({action}[^\"]+)"""",
    """\slevel="({severity}[^\"]+)"""",
    """\slogdesc="({description}[^\"]+)"""",
    """\sdevid="({devid}[^\s]+)"""",
    """\d\d:\d\d:\d\d ({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\b"""
    """\slogid="({log_uid}[^\"]+)"""",
    """ msg="({event_name}[^\"]+)""""
  ]
  DupFields = [ "host->dest_host", "user->account" ]


}
```