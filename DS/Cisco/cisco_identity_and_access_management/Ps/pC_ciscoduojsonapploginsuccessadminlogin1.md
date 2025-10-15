#### Parser Content
```Java
{
Name = cisco-duo-json-app-login-success-adminlogin-1
  Vendor = Cisco
  Product = "Cisco Identity and Access Management"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ duo:""", """|admin_login|""", """"ip_address":""", """"primary_auth_method":""" ]
  Fields = [
    """:\d\d:\d\d ({host}[\w.-]+)\sduo:""",
    """\sduo:\s({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
    """({app}duo)""",
    """\sduo:\s[^\|]+\|({full_name}({first_name}[^\s\|]+)\s({last_name}[^\|]+))""",
    """device":\s*"({object}[^"]+)""",
    """"ip_address":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"primary_auth_method":\s*"({auth_method}[^"]+?)"""",
    """"factor":\s*"({factor}[^"]+?)"""",
    """({event_name}({operation}admin_login))"""
  ]
  ParserVersion = "v1.0.0"


}
```