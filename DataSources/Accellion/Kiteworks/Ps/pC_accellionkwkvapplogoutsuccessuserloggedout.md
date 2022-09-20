#### Parser Content
```Java
{
Name = accellion-kw-kv-app-logout-success-userloggedout
  Vendor = Accellion
  Product = Kiteworks
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """, Activity Group:""", """Activity Type: user_logged_out,""", """Activity: Logged out""" ]
  Fields = [
    """\w+\s+\d+\s\d\d:\d\d:\d\d\s({host}[^\s]+?)\s[^\s]+\s({email_address}[^@]+@({email_domain}[^\s]+))""",
    """id=\d+\s[^\s]+\s({src_ip}[a-fA-F\d\.:]+)""",
    """Activity Type:\s({event_name}user_logged_out)""",
    """Activity:\s({additional_info}Logged out)""",
  ]


}
```