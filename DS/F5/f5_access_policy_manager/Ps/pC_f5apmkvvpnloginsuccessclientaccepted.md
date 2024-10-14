#### Parser Content
```Java
{
Name = f5-apm-kv-vpn-login-success-clientaccepted
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 Access Policy Manager
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = ["""<CLIENT_ACCEPTED>""", """session_id=""", """ip="""]
  Fields = [
    """\d\d:\d\d:\d\d\s+([^\/\s]+\/)?({host}[^\s]+).+?user=({user}[\w\.\-\!\#\^\~]{1,40}\$?).+?session_id=({session_id}[^\s]+)\sip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```