#### Parser Content
```Java
{
Name = "citrix-cgateway-str-vpn-login-success-acessallowed"
Vendor = "Citrix"
Product = "Citrix Gateway"
TimeFormat = "MM/dd/yyyy:HH:mm:ss"
Conditions = [
""" SSLVPN """
"""Access Allowed"""
""" Duration """
""" Total_bytes_send """
]
Fields = [
"""\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s"""
"""\s({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)"""
"""({host}[^\s]+)\s*:\s*SSLVPN \w+\s"""
"""\sEnd_time(\s*\&quot;)?\s*"?({time}\d+\/\d+\/\d+:\d+:\d+:\d+)"""
"""\sUser\s*(({email_address}[^@\-\s]+@[^\.\-\s]+\.[^\-\s]+)|(({domain}[^\\\s\-]+)\\+)?(-|({=email_address}[^@"\s]+@[^@"\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*\-""",
"""({event_name}SSLVPN \w+)"""
"""\sSessionId:\s*({session_id}\d+)"""
"""\sSource\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)"""
"""\sNat_ip\s*({src_translated_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"""
"""\sVserver\s*({dest_translated_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}):({dest_translated_port}\d+)"""
"""\sDestination\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+)"""
"""\sDuration\s*({duration}\d{2}:\d{2}:\d{2})"""
"""\sTotal_bytes_send\s*({bytes_out}\d+)"""
"""\sTotal_bytes_recv\s*({bytes_in}\d+)"""
"""\sAccess\s*({action}[^\s]+)\s"""
"""\sGroup\(s\)\s*("|&quot;)({access_group}[^"]+?)(&quot;|")"""
]
ParserVersion = "v1.0.0"


}
```