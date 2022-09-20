#### Parser Content
```Java
{
Name = f5-apm-kv-vpn-login-success-clientaccepted
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 BIG-IP Access Policy Manager (APM)
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = ["""<CLIENT_ACCEPTED>""", """session_id=""", """ip="""]
  Fields = [
    """\d\d:\d\d:\d\d\s+([^\/\s]+\/)?({host}[^\s]+).+?user=({user}[^\s]+).+?session_id=({session_id}[^\s]+)\sip=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  ]


}
```