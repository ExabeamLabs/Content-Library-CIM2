#### Parser Content
```Java
{
Name = "juniper-ps-kv-vpn-login-success-firewall"
Vendor = "Ivanti"
Product = "Ivanti Pulse Secure"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Session resumed from user agent '"""
"""id=firewall"""
]
Fields = [
"""time="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)".*vpn=({host}[^\s]+).*user=(({email_address}[^@\s\/]+@[^@\s\/]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)).*realm="({realm}[^"]+)?".*roles="({role}[^"]+)?".*src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""({event_code}Session resumed)"""
]
ParserVersion = "v1.0.0"


}
```