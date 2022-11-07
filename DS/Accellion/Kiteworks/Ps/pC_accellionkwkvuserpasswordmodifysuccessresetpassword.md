#### Parser Content
```Java
{
Name = accellion-kw-kv-user-password-modify-success-resetpassword
Vendor = Accellion
Product = Kiteworks
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """, Activity Group:"""
  """Activity Type: reset_password,"""
  """Activity: Reset password"""
]
Fields = [
  """\w+\s+\d+\s\d\d:\d\d:\d\d\s({host}[^\s]+?)\s[^\s]+\s({email_address}[^@]+@({email_domain}[^\s]+))"""
  """id=\d+\s[^\s]+\s({src_ip}[a-fA-F\d\.:]+)"""
  """Activity Type:\s({event_name}reset_password)"""
  """Activity:\s({additional_info}Reset password)"""
]
ParserVersion = "v1.0.0"


}
```