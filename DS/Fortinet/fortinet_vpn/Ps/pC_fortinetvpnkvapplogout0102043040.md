#### Parser Content
```Java
{
Name = fortinet-vpn-kv-app-logout-0102043040
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd 'time='HH:mm:ssZ"
  Conditions = [ """ logid="0102043040" """ ]

fortinet-ssl-vpn-end = {
  Vendor = Fortinet
  Product = Fortinet VPN
  Fields = [
    """({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d([+-]\d\d:\d\d)?)""",
    """\Wdevname="*({host}[\w\-.]+)""",
    """\Wsrcip="*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wuser="(?:N\/A|({user}[^\s@"]+))"""",
    """\Wuser="(?:N\/A|({email_address}[^\s@"]+@[^\s@"]+))"""",
    """\Wstatus="*({action}[^\s"]+)""",
    """\slogdesc="({event_name}[^"]+)""",
    """\smsg="({additional_info}[^"]+)""",
    """\slogid="?({event_code}\d+)"""
  
}
```