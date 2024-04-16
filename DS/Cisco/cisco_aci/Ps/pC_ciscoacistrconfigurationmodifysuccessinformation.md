#### Parser Content
```Java
{
Name = "cisco-aci-str-configuration-modify-success-information"
Vendor = "Cisco"
Product = "Cisco ACI"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""ACI"""
"""modified by"""
"""New: information"""
]
Fields = [
"""\d+:\d+:\d+(.\d+)?\s({host}[^\s]+)"""
"""remoteuser-({user}[\w\.\-]{1,40}\$?)"""
"""info\].+?\s({additional_info}.+?)\s*$"""
]
ParserVersion = "v1.0.0"


}
```