#### Parser Content
```Java
{
Name = accellion-kw-kv-user-lock-success-useraccountlocked
Vendor = Accellion
Product = Kiteworks
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """, Activity Group:"""
  """Activity Type: user_login_lockout,"""
  """Activity: User account locked"""
]
Fields = [
  """\w+\s+\d+\s\d\d:\d\d:\d\d\s({host}[^\s]+?)\s[^\s]+\s({email_address}[^@]+@({email_domain}[^\s]+))"""
  """id=\d+\s[^\s]+\s({src_ip}[a-fA-F\d\.:]+)"""
  """Activity Type:\s({event_name}user_login_lockout)"""
  """Activity:\s({additional_info}User account locked)"""
]
ParserVersion = "v1.0.0"


}
```