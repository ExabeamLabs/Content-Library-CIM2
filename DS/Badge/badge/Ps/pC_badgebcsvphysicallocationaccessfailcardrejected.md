#### Parser Content
```Java
{
Name = "badge-b-csv-physical-location-access-fail-cardrejected"
Vendor = "Badge"
Product = "Badge"
TimeFormat = "yyyy-MM-dd HH:mm:ss a"
Conditions = [
  """,Card Rejected,"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d+:\d+:\d+ (am|AM|PM|pm))"""
  """({result}Rejected),"""
]
ParserVersion = "v1.0.0"


}
```