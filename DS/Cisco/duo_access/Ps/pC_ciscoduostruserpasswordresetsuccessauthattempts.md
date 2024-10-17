#### Parser Content
```Java
{
Name = cisco-duo-str-user-password-reset-success-authattempts
  Vendor = Cisco
  Product = Duo Access
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """ duo: """, """|reset_admin_auth_attempts|""", """": """" ]
  Fields = [
    """"ts"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)""",
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """:\d\d\|({full_name}[^\|]*)\|(|(({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}\w+(\s+\w+)+)))\|({event_name}[^\|]+)\|""",
    """"message":\s*"({additional_info}[^"]+?)"""",
    """({app}duo)""",
   ]


}
```