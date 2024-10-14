#### Parser Content
```Java
{
Name = "f5-apm-cef-vpn-login-success-start"
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = "epoch"
Conditions = [
"""|F5|Big IP|"""
"""Acc-Stat:START"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvchost=\w+\/({host}[\w\-.]+)"""
"""\WUser-Name:\s*(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),"""
"""\WSession-ID:\s*(|({session_id}[^\s,]+)),"""
"""\WTunnel-Client-Endpoint:\s*(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),"""
"""\WFramed-IP-Address:\s*(|({src_translated_ip}[A-Fa-f:\d.]+)),"""
]
ParserVersion = "v1.0.0"


}
```