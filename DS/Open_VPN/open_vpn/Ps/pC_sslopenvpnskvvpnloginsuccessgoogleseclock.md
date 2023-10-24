#### Parser Content
```Java
{
Name = "sslopenvpn-s-kv-vpn-login-success-googleseclock"
Vendor = "Open VPN"
Product = "Open VPN"
TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
Conditions = [
"""] AUTH SUCCESS """
"""pvt_google_auth_secret_locked"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d(\+|\-)\d+).*?AUTH SUCCESS"""
"""'user':\s*.*?'({user}[\w\.\-]{1,40}\$?)',"""
"""auth succeeded on.*?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```