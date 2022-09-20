#### Parser Content
```Java
{
Name = rangeraudit-ra-str-app-login-fail-loginunsuccess
  Vendor = RangerAudit
  Product = RangerAudit
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ranger""", """Login Unsuccessful:""", """Ip Address:""" ]
  Fields = [
    """\[({host}[^\]]+)""",
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """Ip Address:({src_ip}[A-Fa-f:\d.]+)\s*\|\s*({failure_reason}.+?)\s*$""",
    """({app}ranger)""",
  ]
  ParserVersion = v1.0.0


}
```