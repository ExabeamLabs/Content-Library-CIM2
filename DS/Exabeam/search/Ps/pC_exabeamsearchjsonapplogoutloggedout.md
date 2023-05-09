#### Parser Content
```Java
{
Name = exabeam-search-json-app-logout-loggedout
    Vendor = Exabeam
    Product = Search
    ParserVersion = "v1.0.0"
    TimeFormat = "epoch"
    Conditions = [""""Exabeam Audit Event"""", """"event_type":"app-activity"""", """"activity":"Log out""""]
    Fields = [
      """"time":({time}\d{13})""",
      """"host":"({host}[^"]+)""",
      """"src_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"user":"({user}[^"\s]+)""",
      """"activity":"({operation}[^"]+)""",
      """"additional_info":"({additional_info}.+?),?\s*"\}\}""",
      """"app":"({app}[^"]+)""",
    ]
  

}
```