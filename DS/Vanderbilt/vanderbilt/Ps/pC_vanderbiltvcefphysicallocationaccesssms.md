#### Parser Content
```Java
{
Name = "vanderbilt-v-cef-physical-location-access-sms"
Vendor = "Vanderbilt"
Product = "Vanderbilt"
TimeFormat = "epoch"
Conditions = [
  """|Vanderbilt|SMS|"""
]
Fields = [
  """([^\|]*\|){5}({action}[^\|]+)"""
  """\Wrt=({time}\d{13})"""
  """\Wsuid=({user}[^\s]+)"""
  """\Wcs2=({location_building}.+?)\s*(\w+=|$)"""
  """\Wcs5=(\s+|({first_name}.+?))\s*(\w+=|$)"""
  """\Wcs4=(\s+|({last_name}.+?))\s*(\w+=|$)"""
  """\Wad.DeviceCaption=({location_door}.+?)\s*([^\s]+=|$)"""
  """\Wad.CardholderID.l=({badge_id}\d+)"""
  """\Wreason=({result_reason}.+?)\s*(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```