#### Parser Content
```Java
{
Name = "unix-dhcpd-cef-endpoint-login-success-arcsight"
Vendor = "Unix"
Product = "Unix dhcpd"
TimeFormat = "epoch"
Conditions = [
"""|Unix|Unix||arcsight:"""
"""dhcpd"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sdvchost=({host}[\w.\-]+)"""
"""DHCPREQUEST for ({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) from.+?\(({dest_host}[^\)]+)"""
"""Added new forward map from ({dest_host}.+?) to ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),Renewed,({dest_host}[^,]+)"""
]
DupFields = [
"dest_host->user"
]
ParserVersion = "v1.0.0"


}
```