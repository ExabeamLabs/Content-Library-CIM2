#### Parser Content
```Java
{
Name = exabeam-search-cef-app-notification-settings
  Vendor = Exabeam
  Product = Search
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Skyformation-test SIEM settings event""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({event_name}Skyformation-test SIEM settings event)""",
    """msg=({additional_info}.+?)\s*"*$""",
    ]


}
```