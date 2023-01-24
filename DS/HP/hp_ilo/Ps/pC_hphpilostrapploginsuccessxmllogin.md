#### Parser Content
```Java
{
Name = hp-hpilo-str-app-login-success-xmllogin
    ParserVersion = v1.0.0
    Vendor = HP
    Product = HP iLO
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """XML login: """, """ILO""" ]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """\d\d:\d\d:\d\dZ\s({host}[^\s]+)\s\#ILO""",
      """({app}ILO)""",
      """\slogin:\s({user}[^\s]+)""",
      """\slogin:\s(\S+\s){2}({src_ip}[a-fA-F\d:.]+)\(({src_host}[^\)]+)\)"""
      """({event_name}XML login)"""
    ]
    DupFields = ["host->dest_host"]
  

}
```