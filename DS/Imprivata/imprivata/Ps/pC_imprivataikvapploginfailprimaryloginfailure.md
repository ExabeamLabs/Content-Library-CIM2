#### Parser Content
```Java
{
Name = imprivata-i-kv-app-login-fail-primaryloginfailure
  Vendor = Imprivata
  Product = Imprivata
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Event: Primary Login Failure""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[\w\-.]+) ({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """ServerIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """User:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """Event:\s*({operation}.+?)\s+ServerIP:""",
    """({app}Imprivata)""",
  ]
  ParserVersion = v1.0.0


}
```