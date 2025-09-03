#### Parser Content
```Java
{
Name = cisco-mma-str-vpn-login-success-vpnconnect
Vendor = "Cisco"
Product = Cisco Network Security
TimeFormat = "epoch_sec"
Conditions = [
  """ events client_vpn_connect"""
  """connected from """
]
Fields = [
  """({time}\d{10})\.\d{9} \S+\s+events\s"""
  """client_vpn_connect user id \'({user}[\w\.\-\!\#\^\~]{1,40}\$?)\'"""
  """local ip ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """connected from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```