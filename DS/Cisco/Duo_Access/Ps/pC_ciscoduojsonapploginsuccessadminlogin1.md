#### Parser Content
```Java
{
Name = cisco-duo-json-app-login-success-adminlogin-1
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ duo:""", """|admin_login|""", """"ip_address":""", """"primary_auth_method":""" ]
  Fields = [
    """:\d\d:\d\d ({host}[\w.-]+)\sduo:""",
    """\sduo:\s({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
    """({app}duo)""",
    """\sduo:\s[^\|]+\|({full_name}({first_name}[^\s\|]+)\s({last_name}[^\|]+))""",
    """device":\s*"({object}[^"]+)""",
    """"ip_address":\s*"({src_ip}[a-fA-F\d.:]+)"""",
    """"primary_auth_method":\s*"({auth_method}[^"]+?)"""",
    """"factor":\s*"({action}[^"]+?)"""",
    """({operation}admin_login)"""
  ]
  DupFields = ["operation->event_name"]
  ParserVersion = "v1.0.0"


}
```