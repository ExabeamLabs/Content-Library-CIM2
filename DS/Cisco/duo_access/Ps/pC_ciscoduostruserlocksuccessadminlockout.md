#### Parser Content
```Java
{
Name = cisco-duo-str-user-lock-success-adminlockout
  Vendor = Cisco
  Product = Duo Access
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """ duo: """, """|admin_lockout|""", """": """" ]
  Fields = [
    """"ts"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)""",
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """:\d\d\|({full_name}[^\|]*)\|(|({dest_user}[^\|]+))\|({event_name}[^\|]+)\|""",
    """"message":\s*"({additional_info}[^"]+?)"""",
    """({app}duo)"""
  ]


}
```