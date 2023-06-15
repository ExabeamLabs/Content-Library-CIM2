#### Parser Content
```Java
{
Name = shibboleth-s-str-app-login-success-shibbolethaudit
  ParserVersion = v1.0.0
  Vendor = Shibboleth
  Product = Shibboleth
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """[Shibboleth-Audit""" ]
  Fields = [
    """({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+\- \[({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s+\[""",
    """(?:[^\|]*\|){8}({user}[^\|]+)?""",
    """(?:[^\|]*\|){3}({app}[^\|]+)?""",
  ]


}
```