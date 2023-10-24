#### Parser Content
```Java
{
Name = "badgepoint-b-str-physical-location-access-badgepointconditions"
Vendor = "Badgepoint"
Product = "Badgepoint"
TimeFormat = "dd/MM/yyyy:HH:mm:ss z"
Conditions = [
  """<badgepoint_conditions>"""
]
Fields = [
  """([^\|]*\|){6}({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)"""
  """({badge_id}[^\|\s=]+)\|"""
  """([^\|]*\|){1}({last_name}[^\|]+)\|({first_name}[^\|]+)"""
  """([^\|]*\|){3}({location_door}[^\|]+\|[^\|]+)"""
  """([^\|]*\|){5}({action}[^\|]+)"""
]
ParserVersion = "v1.0.0"


}
```