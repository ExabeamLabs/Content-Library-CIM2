#### Parser Content
```Java
{
Name = badge-b-csv-physical-location-access-success-cardexitgranted
  Vendor = Badge
  Product = Badge
  TimeFormat = "dd/MM/yyyy HH:mm:ss a"
  Conditions = [ """"Card Event"""", """"Card Exit Granted"""", """Access Zone""" ]
  Fields = [
    """({time}\d+\/\d+\/\d\d\d\d\s+\d+:\d+:\d+\s+(AM|PM|am|pm)),"Card Event","({action}[^"]+)","({full_name}[^",]+)(,\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?))?\s+exited to Access Zone\s+({location_door}[^"]+?)\s+(({direction}IN|OUT)\s+)?through""",
    """"Card number\s*\(({badge_id}[^\s\)]+)""",
  ]
  DupFields = [ "action->event_name" ]
  ParserVersion = "v1.0.0"


}
```