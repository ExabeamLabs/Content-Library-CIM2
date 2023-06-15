#### Parser Content
```Java
{
Name = dell-sw-kv-vpn-login-success-netextenderconnected
  ParserVersion = v1.0.0
  Product = Sonicwall
  Conditions = [ """msg="NetExtender connected"""", "SSLVPN:", "id=sslvpn"]

sonicwall-vpn-login = {
  Vendor = Dell
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\d\d:\d\d:\d\d ({host}[^\s]+)\sSSLVPN:""",
    """\stime="({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(:({src_interface}[^\s:]+))?(:({src_host}[^\s:]+))?""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?(:({dest_interface}[^\s:]+))?(:({dest_host}[^\s:]+))?""",
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
  DupFields = ["user->account"
}
```