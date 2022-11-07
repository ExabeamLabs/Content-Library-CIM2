#### Parser Content
```Java
{
Name = dell-rsaauthmngr-csv-user-lock-success-authlockout
  Vendor = Dell
  Product = RSA Authentication Manager
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """,AUTHN_LOCKOUT_EVENT,""", """,SUCCESS,""" ]
  Fields = [
    """,({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),AUTHN_LOCKOUT_EVENT""",
    """,({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),AUTHN_LOCKOUT_EVENT""",
    """,({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),[^,]*,AUTHN_LOCKOUT_EVENT""",
    """AUTHN_LOCKOUT_EVENT,([^,]*,){7}({user}[^,]+)""",
    """AUTHN_LOCKOUT_EVENT,([^,]*,){12}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """AUTHN_LOCKOUT_EVENT,([^,]*,){13}({dest_host}[^.,]+)""",
    """AUTHN_LOCKOUT_EVENT,([^,]*,){13}[^.,]+\.({domain}[^.,]+)""",
    """AUTHN_LOCKOUT_EVENT,([^,]*,){16}({auth_method}[^.,]+)"""
  ]


}
```