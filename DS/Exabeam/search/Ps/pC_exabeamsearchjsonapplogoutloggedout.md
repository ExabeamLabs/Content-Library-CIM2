#### Parser Content
```Java
{
Name = exabeam-search-json-app-logout-loggedout
  Vendor = Exabeam
  Product = Search
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """"Exabeam Audit Event"""", """"event_type":"app-activity"""", """"activity":"Log out"""" ]
  Fields = [
    """"time":({time}\d{13})""",
    """"host":"({host}[^"]+)""",
    """"src_ip":"({src_ip}[A-Fa-f:\d.]+)""",
    """"user":"({user}[^"\s]+)""",
    """"activity":"({operation}[^"]+)""",
    """"additional_info":"({additional_info}.+?),?\s*"\}\}""",
    """"app":"({app}[^"]+)""",
  ]


}
```