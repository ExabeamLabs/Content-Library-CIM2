#### Parser Content
```Java
{
Name = "badge-b-json-physical-location-access-fail-badge"
Vendor = "Badge"
Product = "Badge"
TimeFormat = "epoch_sec"
Conditions = [
  """BADGE"""
  """Floor"""
]
Fields = [
  """(?:([^\|]*\|))\s+({time}\d{10})"""
  """(?:([^\|]*\|)){3}\s+({last_name}[^,\|]+),\s+({first_name}[^\|]+)\s+\|"""
  """(?:([^\|]*\|)){4}\s+({action}[^\|]+)\s+\|"""
  """(?:([^\|]*\|)){5}\s+\d+\s+-\s*({location_city}[^-]+)\s+-({location_door}[^\|]+)\s+\|"""
  """(?:([^\|]*\|)){6}\s+({location_building}.+?)\s+$"""
]
ParserVersion = "v1.0.0"


}
```