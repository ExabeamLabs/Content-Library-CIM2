#### Parser Content
```Java
{
Name = shibboleth-s-str-app-login-success-shibbolethaudit
  ParserVersion = v1.0.0
  Vendor = Shibboleth
  Product = Shibboleth
  TimeFormat = [ "yyyy-MM-dd HH:mm:ss", "yyyyMMdd'T'HHmmssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ" ]
  Conditions = [ """[Shibboleth-Audit""" ]
  Fields = [
    """\]\s*({time}\d{8}T\d{6}Z)""",
    """\]\s*\-\s*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
    """({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+\- \[({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s+\[""",
    """(?:[^\|]*\|){8}(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """(?:[^\|]*\|){3}({app}[^\|]+)?""",
  ]


}
```