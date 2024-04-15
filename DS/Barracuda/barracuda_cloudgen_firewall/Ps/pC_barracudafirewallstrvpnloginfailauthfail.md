#### Parser Content
```Java
{
Name = "barracuda-firewall-str-vpn-login-fail-authfail"
Vendor = "Barracuda"
Product = "Barracuda Cloudgen Firewall"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Session PHS:"""
""" authentication failed:"""
"""Authentication failed"""
""" Login """
]
Fields = [
  """Security\s+({host}[^\s:]+)\s+Session"""
  """Authentication failed\s*\(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)"""
  """Login\s+'(({email_address}[^'@\(]+@[^'\(@]+)|({user}[^\s']+))'"""
  """Session PHS:\s*({event_name}[^:=\(]+?)\s*(:|\w+=|\(|$)"""
  """({result}failed)"""
 ]
ParserVersion = "v1.0.0"


}
```