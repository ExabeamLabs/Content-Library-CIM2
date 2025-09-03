#### Parser Content
```Java
{
Name = accellion-kw-kv-group-member-add-adduser
  Vendor = Accellion
  Product = Kiteworks
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """, Activity Group:""", """Activity Type: add_user,""", """Activity: Added new standard User""" ]
  Fields = [
    """\w+\s+\d+\s\d\d:\d\d:\d\d\s({host}[^\s]+?)\s[^\s]+\s({email_address}[^@]+@({email_domain}[^\s]+\.[^\]\s"\\,\|]+))""",
    """id=\d+\s[^\s]+\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Activity Type:\s({event_name}add_user)""",
    """Activity:\s({additional_info}Added new standard User)""",
  ]


}
```