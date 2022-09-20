#### Parser Content
```Java
{
Name = accellion-kw-kv-user-unlock-success-reactivateuser
Vendor = Accellion
Product = Kiteworks
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """, Activity Group:"""
  """Activity Type: reactivate_user"""
  """Activity: User reactivated:"""
]
Fields = [
  """\w+\s+\d+\s\d\d:\d\d:\d\d\s({host}[^\s]+?)\s[^\s]+\s({email_address}[^@]+@({email_domain}[^\s]+))"""
  """id=\d+\s[^\s]+\s({src_ip}[a-fA-F\d\.:]+)"""
  """Activity Type:\s({event_name}reactivate_user)"""
  """Activity:\s({additional_info}User reactivated)"""
]
ParserVersion = "v1.0.0"


}
```