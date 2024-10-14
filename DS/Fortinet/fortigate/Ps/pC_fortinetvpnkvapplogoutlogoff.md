#### Parser Content
```Java
{
Name = "fortinet-vpn-kv-app-logout-logoff"
  Vendor = "Fortinet"
  Product = "FortiGate"
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd 'time='HH:mm:ss"
  Conditions = [ """action="FSSO-logoff""", """ logdesc=""" ]
  Fields = [
    """date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d)""",
    """devname="*({host}[^"]+?)"*(\s+\w+=|\s*$)""",
    """\ssrcip="?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sdstip="?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\suser="*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"*(\s+\w+=|\s*$)""",
    """\sreason="(Authentication succeeded|({failure_reason}[^"]+))"""",
    """\slogdesc="({event_name}[^"]+)""",
    """\sserver="({dest_host}[^"]+)""",
  ]


}
```