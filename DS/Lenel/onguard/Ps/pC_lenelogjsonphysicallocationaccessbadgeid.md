#### Parser Content
```Java
{
Name = "lenel-og-json-physical-location-access-badgeid"
Vendor = "Lenel"
Product = "OnGuard"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """"cardholder_first_name":"""
  """"badge_id":"""
]
Fields = [
  """"timestamp\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)"""
  """"badge_id\":({badge_id}\d+)"""
  """"cardholder_first_name\":\"({first_name}[^\"]+)"""
  """"cardholder_last_name\":\"({last_name}[^\"]+)"""
  """"device_name\":\"({location_door}[^\"]+)"""
  """"description\":\"({action}[^\"]+)"""
]
ParserVersion = "v1.0.0"


}
```