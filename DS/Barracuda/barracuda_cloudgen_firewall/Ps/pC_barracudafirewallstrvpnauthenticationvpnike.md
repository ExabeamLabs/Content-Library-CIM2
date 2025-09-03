#### Parser Content
```Java
{
Name = "barracuda-firewall-str-vpn-authentication-vpnike"
Vendor = "Barracuda"
ParserVersion = "v1.0.0"
Product = "Barracuda Cloudgen Firewall"
TimeFormat = "MMM dd HH:mm:ss"
Conditions = [
  """/srv_CSC_VPN_IKEv2:"""
]
Fields = [
  """({time}\w+\s\d+\s\d\d:\d\d:\d\d)\s({host}[\w\_\.]+)\s\w+\/({event_name}srv_CSC_VPN_IKEv2):\s*({additional_info}.+?)\s*($)"""
]


}
```