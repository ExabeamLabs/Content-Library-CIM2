#### Parser Content
```Java
{
Name = fortinet-vpn-kv-app-authentication-fail-0102043011
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd 'time='HH:mm:ss"
  Conditions = [ """ logid="0102043011" """ ]
  Fields = ${DLFortinetParsersTemplates.fortinet-ssl-vpn-end.Fields} [
    """\Wstatus="*({failure_code}[^\s"]+)"""",
    """\slogdesc="({failure_reason}[^"]+)""",
  ]

fortinet-ssl-vpn-end = {
  Vendor = Fortinet
  Product = FortiGate
  Fields = [
    """({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """date=({time}\d\d\d\d\-\d\d\-\d\d time\=\d\d:\d\d:\d\d)""",
    """\Wdevname="*({host}[\w\-.]+)""",
    """\Wsrcip="*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wuser="(?:N\/A|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """\Wuser="(?:N\/A|({email_address}[^\s@"]+@[^\s@"]+))"""",
    """\Wstatus="*({action}[^\s"]+)""",
    """\slogdesc="({event_name}[^"]+)""",
    """\smsg="({additional_info}[^"]+)""",
    """\slogid="?({event_code}\d+)""",
    """\Wtz="?({tz}[+-]\d+)"""
  
}
```