#### Parser Content
```Java
{
Name = "kabaexos-k-cef-physical-location-access-success-9300"
Vendor = "KABA EXOS"
Product = "KABA EXOS"
TimeFormat = "epoch"
Conditions = [
"""|KABA|EXOS 9300|"""
]
Fields = [
"""([^\|]*\|){5}({action}[^\|]+)"""
"""\Wrt=({time}\d{13})"""
"""\Wduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\Wmsg=({location_door}.+?)\s*(\w+=|$)"""
"""\Wcs2=({badge_id}\d+)"""
]
ParserVersion = "v1.0.0"


}
```