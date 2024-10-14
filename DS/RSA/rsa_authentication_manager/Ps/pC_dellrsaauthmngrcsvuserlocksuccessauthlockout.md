#### Parser Content
```Java
{
Name = dell-rsaauthmngr-csv-user-lock-success-authlockout
  Vendor = RSA
  Product = RSA Authentication Manager
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """,AUTHN_LOCKOUT_EVENT,""", """,SUCCESS,""" ]
  Fields = [
    """,({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),AUTHN_LOCKOUT_EVENT""",
    """,({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,AUTHN_LOCKOUT_EVENT""",
    """,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),[^,]*,AUTHN_LOCKOUT_EVENT""",
    """AUTHN_LOCKOUT_EVENT,([^,]*,){7}({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """AUTHN_LOCKOUT_EVENT,([^,]*,){12}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """AUTHN_LOCKOUT_EVENT,([^,]*,){13}({dest_host}[^.,]+)""",
    """AUTHN_LOCKOUT_EVENT,([^,]*,){13}[^.,]+\.({domain}[^.,]+)""",
    """AUTHN_LOCKOUT_EVENT,([^,]*,){16}({auth_method}[^.,]+)"""
  ]


}
```