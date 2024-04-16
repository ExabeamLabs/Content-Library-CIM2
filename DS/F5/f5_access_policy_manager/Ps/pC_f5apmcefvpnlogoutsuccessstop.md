#### Parser Content
```Java
{
Name = "f5-apm-cef-vpn-logout-success-stop"
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = "epoch"
Conditions = [
"""|F5|Big IP|"""
"""Acc-Stat:STOP"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvchost=\w+\/({host}[\w\-.]+)"""
"""\WUser-Name:\s*(|({user}[\w\.\-]{1,40}\$?)),"""
"""\WSession-ID:\s*(|({session_id}[^\s,]+)),"""
"""\WFramed-IP-Address:\s*(|({src_translated_ip}[A-Fa-f:\d.]+)),"""
]
ParserVersion = "v1.0.0"


}
```