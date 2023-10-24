#### Parser Content
```Java
{
Name = "avaya-vpn-kv-vpn-login-success-vpnsuccess"
Vendor = "Avaya"
Product = "Avaya VPN"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
""" LoginSucceeded """
"""avaya:vpn"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w.\-]+)\s+SSL:"""
"""\sSrcIp=\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sUser=\"(({domain}[^\\\"]+)\\+)?({user}[\w\.\-]{1,40}\$?)"""
"""\sGroups=\"({realm}[^\"]+?)\/?\s*\""""
"""\sTunIP=\"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```