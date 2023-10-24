#### Parser Content
```Java
{
Name = "icpam-i-kv-physical-location-access-success-granted"
Vendor = "ICPAM"
Product = "ICPAM"
TimeFormat = ["MM/dd/yyyy HH:mm:ss","M/dd/yyyy HH:mm:ss"]
Conditions = [
  """[Connected Physical Access Manager]"""
  """Trigger:"""
]
Fields = [
  """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[^\s]+)"""
  """Time:\s*({time}\d+/\d+/\d\d\d\d \d\d:\d\d:\d\d)"""
  """Trigger:\s*({action}.+?)\s*(#012|Time)"""
  """Device:\s*({location_door}.+?)\s+(#012|Personnel)"""
  """Badge Id\s*:\s*({badge_id}\d+\s*\d+)"""
  """Personnel record:\s*({last_name}.+?)\s*,\s+({first_name}.+?)\s*(#012|Credential)"""
]
ParserVersion = "v1.0.0"


}
```