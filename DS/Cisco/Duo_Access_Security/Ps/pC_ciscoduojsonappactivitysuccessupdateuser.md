#### Parser Content
```Java
{
Name = cisco-duo-json-app-activity-success-updateuser
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Duo Access Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ duo: """, """|user_update|""", """": """" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """:\d\d\|({full_name}[^\|]*)\|(|({dest_user}[^\|]+))\|({operation}[^\|]+)\|""",
    """"email":\s*"({email_address}[^@"]+@({email_domain}[^"\s]+))"""",
    """({app}duo)"""
  ]


}
```