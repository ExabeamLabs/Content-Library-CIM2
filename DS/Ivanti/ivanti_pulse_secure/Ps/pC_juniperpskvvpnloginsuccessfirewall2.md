#### Parser Content
```Java
{
Name = "juniper-ps-kv-vpn-login-success-firewall-2"
Vendor = "Ivanti"
Product = "Ivanti Pulse Secure"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""PulseSecure:"""
"""Remote address for user"""
"""id=firewall"""
]
Fields = [
"""time="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)".*vpn=({host}[^\s]+).*user=(({email_address}[^@\s\/]+@[^@\s\/]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)).*realm="({realm}[^"]+)?".*roles="({role}[^"]+)?".*changed from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? to ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
]
ParserVersion = "v1.0.0"


}
```