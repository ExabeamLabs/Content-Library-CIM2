#### Parser Content
```Java
{
Name = hp-hpilo-str-app-logout-success-browserlogout
  Conditions = [ """Browser logout: """, """ILO""" ]
  Fields = ${DLHPEParsersTemplates.hp-ilo-app-logout.Fields} [
    """({event_name}Browser logout)"""
  ]
  ParserVersion = "v1.0.0"

hp-ilo-app-logout = {
    Vendor = HP
    Product = HP iLO
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """\d\d:\d\d:\d\dZ\s({host}[^\s]+)\s#ILO""",
      """({app}ILO)""",
      """\slogout:\s({user}[^\s]+)""",
      """\slogout:\s(\S+\s){2}({src_ip}[a-fA-F\d:.]+)\(({src_host}[^\)]+)\)"""
    ]
    DupFields = ["host->dest_host"
}
```