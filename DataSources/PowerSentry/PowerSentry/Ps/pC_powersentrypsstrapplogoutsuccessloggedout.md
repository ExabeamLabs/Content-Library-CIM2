#### Parser Content
```Java
{
Name = powersentry-ps-str-app-logout-success-loggedout
  Vendor = PowerSentry
  Product = PowerSentry
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ [Sentry""", """" logged out --""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[^\s]+) \[({src_host}[^\]]+)\].+?User "({user}[^\s"]+)""",
    """connection source ({src_ip}[A-Fa-f:\d.]+) using ({protocol}[^\s]+)""",
  ]


}
```