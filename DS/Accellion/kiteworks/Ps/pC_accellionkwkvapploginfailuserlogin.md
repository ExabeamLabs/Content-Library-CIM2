#### Parser Content
```Java
{
Name = accellion-kw-kv-app-login-fail-userlogin
  ParserVersion = v1.0.0
  Vendor = Accellion
  Product = Kiteworks
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """, Activity Group:""", """Activity Type: user_login_failed""", """login failed""" ]
  Fields = [
    """\w+\s+\d+\s\d\d:\d\d:\d\d\s({host}[^\s]+?)\s[^\s]+([^=]+=[^,]+,)?\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """User:\s+(({email_address}[^@\s]+@({email_domain}[^\s\.]+\.[^\s]+))|({user}[^\s@]+)(@({domain}[^\s]+))?)\s({additional_info}login failed)""",
    """Activity Type:\s({event_name}user_login_failed)""",
  ]


}
```