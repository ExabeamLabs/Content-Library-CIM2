#### Parser Content
```Java
{
Name = "dell-sw-str-vpn-login-success-csacl"
Vendor = "Dell"
Product = "Sonicwall"
TimeFormat = "dd/MMM/yyyy:HH:mm:ss"
Conditions = [
"""matched rule #"""
"""is permitted"""
"""CSACL"""
]
Fields = [
""":\s.+?\]\s+({host}[^\s]+).+?\sUser.+?\(({user}[^\)]+).+connecting from.+?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):.+access to.+?({dest_host}[\w.-]+)"""
]
ParserVersion = "v1.0.0"


}
```