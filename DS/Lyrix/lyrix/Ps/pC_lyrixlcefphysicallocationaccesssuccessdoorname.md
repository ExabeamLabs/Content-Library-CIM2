#### Parser Content
```Java
{
Name = "lyrix-l-cef-physical-location-access-success-doorname"
Vendor = "Lyrix"
Product = "Lyrix"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|SKUD|"""
  """cs2Label=DoorName"""
]
Fields = [
  """CEF:([^\|]*\|){5}({action}[^\|]+)"""
  """\Wdvc=({host}[A-Fa-f:\d.]+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wrt=({time}\d{13})"""
  """\Wcs3=({direction}.+?)\s+(\w+=|$)"""
  """\Wcs2=({location_door}.+?)\s+(\w+=|$)"""
  """\Wcs1=({location_building}.+?)\s+(\w+=|$)"""
  """\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\Wsuid=({full_name}.+?)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```