#### Parser Content
```Java
{
Name = imprivata-i-kv-app-login-success-primaryloginsuccess
  Vendor = Imprivata
  Product = Imprivata
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Event: Primary Login Success""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[\w\-.]+) ({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """ServerIP:\s*({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """User:\s*({user}[^\s\#]+)""",
    """Event:\s*({operation}.+?)\s+ServerIP:""",
    """({app}Imprivata)""",
  ]
  ParserVersion = v1.0.0


}
```