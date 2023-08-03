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
      """\slogout:\s({user}[\w\.\-]{1,40}\$?)""",
      """\slogout:\s(\S+\s){2}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\(({src_host}[^\)]+)\)"""
    ]
    DupFields = ["host->dest_host"
}
```