#### Parser Content
```Java
{
Name = accellion-kw-kv-user-unlock-success-useraccountunlocked
Vendor = Accellion
Product = Kiteworks
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """, Activity Group:"""
  """Activity Type: user_login_unlock,"""
  """Activity: User account unlocked"""
]
Fields = [
  """\w+\s+\d+\s\d\d:\d\d:\d\d\s({host}[^\s]+?)\s[^\s]+\s({email_address}[^@]+@({email_domain}[^\s]+))"""
  """id=\d+\s[^\s]+\s({src_ip}[a-fA-F\d\.:]+)"""
  """Activity Type:\s({event_name}[^,]+?),"""
  """Activity:\s({additional_info}User account unlocked by lockout cooldown)"""
]
ParserVersion = "v1.0.0"


}
```