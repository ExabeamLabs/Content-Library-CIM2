#### Parser Content
```Java
{
Name = "lyrix-l-cef-physical-location-access-success-department"
Vendor = "Lyrix"
Product = "Lyrix"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Lyrix|"""
  """|SKUD"""
  """cs3Label=DEPARTMENT"""
]
Fields = [
  """\Wact=({action}.+?)\s+\w+="""
  """\Wcs1=({badge_id}.+?)\s+(\w+=|$)"""
  """\Wcs6=({location_door}.+?)\s+(\w+=|$)"""
  """\Wcs3=({location_building}.+?)\s+(\w+=|$)"""
  """ flexString1=({location_city}.+?)\s+\S+="""
  """ flexString2=({additional_info}.+?)\s+\S+="""
  """\Wdvc=({host}[A-Fa-f:\d.]+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wrt=({time}\d{13})"""
  """\Wsuser=({user}.+?)\s+(\w+=|$)"""
]
DupFields = [
  "user->full_name"
]
ParserVersion = "v1.0.0"


}
```