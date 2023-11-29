#### Parser Content
```Java
{
Name = "amag-sac-kv-physical-location-access-eventcode"
Vendor = "AMAG"
Product = "Symmetry Access Control"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
""" Device: """
""" EventCode: """
""" OPR: """
]
Fields = [
  """Date:\s*({time}\d+\/\d+\/\d\d\d\d\s+\d+:\d+:\d+\s+(AM|PM|am|pm)) Device:\s*({location_door}.+?)\s+EventCode:\s*({action}\d+)\s+Name:\s*(|({full_name}[^:]*?))\s+OPR:\s*(|({operation}.+?))\s*(\d{4}\-|"|$|\w+=)"""
]
ParserVersion = "v1.0.0"


}
```