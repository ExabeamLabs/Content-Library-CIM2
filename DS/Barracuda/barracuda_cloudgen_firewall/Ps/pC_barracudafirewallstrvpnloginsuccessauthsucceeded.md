#### Parser Content
```Java
{
Name = "barracuda-firewall-str-vpn-login-success-authsucceeded"
Vendor = "Barracuda"
Product = "Barracuda Cloudgen Firewall"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Session PHS:"""
""" authentication succeeded:"""
""" Login """
]
Fields = [
  """Info\s+({host}[^\s:]+)\s+Session"""
  """\W(login|user)=(({email_address}[^@\(]+@[^\(@]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)"""
  """Login\s+'(({email_address}[^'@\(]+@[^'\(@]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'"""
  """Session PHS:\s*({event_name}[^:=\(]+?)\s*(:|\w+=|\(|$)"""
  """({result}succeeded)"""
 ]
DupFields = [
"user->account"
]
ParserVersion = "v1.0.0"


}
```