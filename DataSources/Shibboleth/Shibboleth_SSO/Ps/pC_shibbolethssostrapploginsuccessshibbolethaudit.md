#### Parser Content
```Java
{
Name = shibboleth-sso-str-app-login-success-shibbolethaudit
  ParserVersion = v1.0.0
  Vendor = Shibboleth
  Product = Shibboleth SSO
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """[Shibboleth-Audit""" ]
  Fields = [
    """({src_ip}[a-fA-F\d.:]+)\s*$""",
    """({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+\- \[({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s+\[""",
    """(?:[^\|]*\|){8}({user}[^\|]+)?""",
    """(?:[^\|]*\|){3}({app}[^\|]+)?""",
  ]


}
```