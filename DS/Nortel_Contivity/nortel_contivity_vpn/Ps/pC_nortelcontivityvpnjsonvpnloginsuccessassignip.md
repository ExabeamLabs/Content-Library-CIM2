#### Parser Content
```Java
{
Name = "nortelcontivity-vpn-json-vpn-login-success-assignip"
Vendor = "Nortel Contivity"
Product = "Nortel Contivity VPN"
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
"""tEvtLgMgr"""
"""assigned IP address"""
]
Fields = [
"""\w+\s+\d+ \d+:\d+:\d+ ({host}[\w.\-]+)"""
"""({time}\d+/\d+/\d+ \d+:\d+:\d+)"""
"""\[({user}[\w\.\-]{1,40}\$?)\]:({contivity_session_id}\d+) assigned IP address ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
]
ParserVersion = "v1.0.0"


}
```