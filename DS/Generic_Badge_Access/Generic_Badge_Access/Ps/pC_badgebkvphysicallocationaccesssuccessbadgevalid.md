#### Parser Content
```Java
{
Name = badge-b-kv-physical-location-access-success-badgevalid
  Vendor = Generic Badge Access
  Product = Generic Badge Access
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """"BADGE VALID""""]
  Fields = [
    """AckTStamp=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)""",
    """Description:\s*"*({last_name}[^,"]+),\s+({first_name}[^,"]+)""",
    """Badge:\s*"*({badge_id}[^"]+)""",
    """Class:\s*"*({action}[^"]+)""",
    """Name:\s*"*({location_full}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```