#### Parser Content
```Java
{
Name = hp-hpilo-str-app-login-success-browserlogin
    ParserVersion = v1.0.0
    Vendor = HP
    Product = HP iLO
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """Browser login: """, """ILO""" ]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """\d\d:\d\d:\d\dZ\s({host}[^\s]+)\s\#ILO""",
      """({app}ILO)""",
      """\slogin:\s({user}[^\s]+)""",
      """\slogin:\s(\S+\s){2}({src_ip}[a-fA-F\d:.]+)\(({dest_host}[^\)]+)\)"""
      """({event_name}Browser login)"""
    ]


}
```