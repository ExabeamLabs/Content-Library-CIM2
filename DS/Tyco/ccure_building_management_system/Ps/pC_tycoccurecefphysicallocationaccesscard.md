#### Parser Content
```Java
{
Name = "tyco-ccure-cef-physical-location-access-card"
Vendor = "Tyco"
Product = "CCURE Building Management System"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|C-CURE|"""
  """|Card"""
]
Fields = [
  """src=({host}[^\s]+)"""
  """({action}Card (Rejected|Admitted))"""
  """\|start=({time}\d{13})"""
  """\ssuid=(?:Unknown|(({domain}[^\\]+)\\?)?({user}.+?))\s(\w+=|$)"""
  """\ssuser=(?:|({full_name}.+?))\s(\w+=|$)"""
  """\scs1=(?:|({location_door}.+?))\s(\w+=|$)"""
  """\scs3=(?:|({location_city}.+?))\s(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```