#### Parser Content
```Java
{
Name = cisco-duo-json-user-create-success-usercreate
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ duo: """, """|user_create|""", """": """" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """:\d\d\|({full_name}[^\|]*)\|(|({dest_user}[^\|]+))\|({operation}[^\|]+)\|""",
    """"email":\s*"({email_address}[^@"]+@({email_domain}[^"\s]+))"""",
    """({app}duo)"""
  ]
  DupFields = [ "dest_user->account_name" ]


}
```