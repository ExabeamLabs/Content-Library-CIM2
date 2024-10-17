#### Parser Content
```Java
{
Name = "cisco-ise-kv-vpn-logout-success-virtual"
Vendor = "Cisco"
Product = "Cisco ISE"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
ParserVersion = "v1.0.0"
Conditions = [
"""CSCOacs_RADIUS_Accounting"""
"""RADIUS Accounting stop request,"""
"""Acct-Status-Type=Stop"""
"""NAS-Port-Type=Virtual"""
]
Fields = [
"""\d+\s+({time}\d\d\d\d\-\d\d\-\d\d \d+:\d+:\d+)"""
"""CSCOacs_RADIUS_Accounting\s+(\d+\s+){3}\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""({host}[^\s]+)\s+CSCOacs_RADIUS_Accounting"""
""",\s*User-Name =(({domain}[^\s\\\/]+)[\\\/]+)?(?:(\w{2}\-){5}\w{2}|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""Tunnel-Client-Endpoint=\(.+?\)\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""Framed-IP-Address=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),"""
"""\:\d\d\s+({dest_host}[\w\-.]+?)\sCSCOacs"""
""",\s*Device IP Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""Acct-Output-Octets=({bytes_in}\d+),"""
"""Acct-Input-Octets=({bytes_out}\d+),"""
"""Acct-Session-Time=({session_duration}\d+),"""
"""Acct-Terminate-Cause=({additional_info}.*?),\sNAS-Port"""
]


}
```