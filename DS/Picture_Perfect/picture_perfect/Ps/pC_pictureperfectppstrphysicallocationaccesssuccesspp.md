#### Parser Content
```Java
{
Name = "pictureperfect-pp-str-physical-location-access-success-pp"
Vendor = "Picture Perfect"
Product = "Picture Perfect"
TimeFormat = "yyyyMMdd|HHmmss"
Conditions = [
  """pictureperfect"""
]
Fields = [
  """^[^|]*?\|([^|]*\|){2}({user}[\w\.\-\!\#\^\~]{1,40}\$?)\|"""
  """^[^|]*?\|([^|]*\|){3}({first_name}[^|]+)\|"""
  """^[^|]*?\|([^|]*\|){4}({last_name}[^|]+)\|"""
  """^[^|]*?\|([^|]*\|){12}({location_full}[^|]+)\|"""
  """^[^|]*?\|([^|]*\|){12}[^|]*\s({direction}(?:IN|OUT))\s[^|]*\|"""
  """^[^|]*?\|([^|]*\|){15}({time}\d{8}\|\d{6})\|"""
]
DupFields = [
  "location_full->location_door"
]
ParserVersion = "v1.0.0"


}
```