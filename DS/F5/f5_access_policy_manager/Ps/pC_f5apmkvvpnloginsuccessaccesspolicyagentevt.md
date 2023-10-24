#### Parser Content
```Java
{
Name = f5-apm-kv-vpn-login-success-accesspolicyagentevt
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 Access Policy Manager
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = ["""<ACCESS_POLICY_AGENT_EVENT>""", """session_id=""", """vpngroup="""]
  Fields = [
  """\d\d:\d\d:\d\d\s+([^\/\s]+\/)?({host}[^\s]+).+?access_type=({vpn_type}[^\s]+)\suser=({user}[\w\.\-]{1,40}\$?).+?vpngroup=({realm}[^\s]+)\ssession_id=({session_id}[^\s]+)\s*$"""
  ]


}
```