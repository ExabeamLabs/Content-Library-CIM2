#### Parser Content
```Java
{
Name = "nortelcontivity-vpn-json-vpn-login-success-address"
Vendor = "Nortel Contivity"
Product = "Nortel Contivity VPN"
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
"""tEvtLgMgr"""
"""physical addresses:"""
]
Fields = [
"""\w+\s+\d+ \d+:\d+:\d+ ({host}[\w.\-]+)"""
"""({time}\d+/\d+/\d+ \d+:\d+:\d+)"""
"""\[({user}[\w.'\-]+)\]:({contivity_session_id}\d+)"""
"""physical addresses: remote ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) local ({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```