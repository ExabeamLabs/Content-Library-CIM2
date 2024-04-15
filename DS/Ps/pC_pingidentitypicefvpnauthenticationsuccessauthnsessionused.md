#### Parser Content
```Java
{
Name = "pingidentity-pi-cef-vpn-authentication-success-authnsessionused"
Conditions = [
"""CEF"""
"""|Ping Identity|PingFederate|"""
"""|AUTHN_SESSION_USED|AUTHN_SESSION_USED|"""
"""msg=success"""
]
ParserVersion = "v1.0.0"

sonicwall-vpn-login = {
  Vendor = Dell
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\d\d:\d\d:\d\d ({host}[^\s]+)\sSSLVPN:""",
    """\stime="({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
    """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(:({src_port}\d+))?(:({src_interface}[^\s:]+))?(:({src_host}[^\s:]+))?""",
    """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(:({dest_port}\d+))?(:({dest_interface}[^\s:]+))?(:({src_host}[^\s:]+))?""",
    """\suser="\s*(({email_address}[^@"]+@[^\\\s"]+)|({user}[^\\\s"]+))""",
    """\susr="\s*(({email_address}[^@"]+@[^\\\s"]+)|({user}[^\\\s"]+))\s*"""",
    """\sproto=({protocol}\S+)""",
    """\sdomain="({domain}[^"]+)"""",
    """\sportal="({realm}[^"]+)"""",
    """\sagent="({user_agent}[^"]+)"""",
    """\sduration=({session_duration}\d+)""",
    """\sbytesIn=({bytes_in}\d+)""",
    """\sbytesOut=({bytes_out}\d+)""",
    """\sbytesTotal=({bytes}\d+)"""
  ]
  DupFields = ["user->account"]
  ParserVersion = "v1.0.0"

}
```