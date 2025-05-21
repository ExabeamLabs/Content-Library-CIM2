#### Parser Content
```Java
{
Name = "cisco-asa-kv-vpn-login-success-user"
Vendor = "Cisco"
Product = "Cisco Network Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""DAP: User"""
"""endpoint.device.hostname"""
]
Fields = [
"""DAP: User (({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
""", Addr ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?: Session"""
"""endpoint.device.hostname="*({src_host}[^"\s]+)"""
]
DupFields = [
"user->account"
]
ParserVersion = "v1.0.0"


}
```