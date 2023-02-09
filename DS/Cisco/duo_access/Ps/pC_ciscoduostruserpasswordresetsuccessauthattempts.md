#### Parser Content
```Java
{
Name = cisco-duo-str-user-password-reset-success-authattempts
  Vendor = Cisco
  Product = Duo Access
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ duo: """, """|reset_admin_auth_attempts|""", """": """" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """:\d\d\|({full_name}[^\|]*)\|(|({dest_user}[^\|]+))\|({event_name}[^\|]+)\|""",
    """"message":\s*"({additional_info}[^"]+?)"""",
    """({app}duo)""",
   ]


}
```