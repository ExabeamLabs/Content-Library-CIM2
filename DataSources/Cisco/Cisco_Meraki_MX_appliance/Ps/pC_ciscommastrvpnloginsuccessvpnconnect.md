#### Parser Content
```Java
{
Name = cisco-mma-str-vpn-login-success-vpnconnect
Vendor = "Cisco"
Product = "Cisco Meraki MX appliance"
TimeFormat = "epoch_sec"
Conditions = [
  """ events client_vpn_connect"""
  """connected from """
]
Fields = [
  """({time}\d{10})\.\d{9} \S+\s+events\s"""
  """client_vpn_connect user id \'({user}[^']+)\'"""
  """local ip ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """connected from ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
]
ParserVersion = "v1.0.0"


}
```