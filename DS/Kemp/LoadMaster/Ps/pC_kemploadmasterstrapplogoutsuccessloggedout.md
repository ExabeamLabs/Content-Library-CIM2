#### Parser Content
```Java
{
Name = kemp-loadmaster-str-app-logout-success-loggedout
  Vendor = Kemp
  Product = LoadMaster
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """logger: User""", """ Logged out """ ]
  Fields = [
    """User\s+({user}.+?)\s+\(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\)""",
    """({event_name}Logged out)""",
    """({event_category}logger)"""
  ]


}
```