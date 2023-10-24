#### Parser Content
```Java
{
Name = "redcloud-aacm-cef-physical-location-access-credential"
Vendor = "Aviglion"
Product = "Aviglion ACM"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|RedCloud|Enterprise|"""
"""Credential"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\|(?:([^\|]*\|)){4}({action}[^\|]+)"""
"""\scat=({category}.+?)\s+\w+="""
"""\sduser=({last_name}[^,]+),({first_name}.+?)\s+\w+="""
"""\scs1=({location_building}.+?)\s+\w+="""
"""\scs5=({location_door}.+?)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```