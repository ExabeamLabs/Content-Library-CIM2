#### Parser Content
```Java
{
Name = "tyco-ccure-cef-physical-location-access-fail-ccurebadge"
Vendor = "Tyco"
Product = "CCURE Building Management System"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Software House|CCure Badge|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sduser=\s*({last_name}[^,]+?)\s*,\s*({first_name}.+?)(\s+\w+=|\s*$)"""
"""\scs3=({location_door}.+?)(\s+\w+=|\s*$)"""
"""\|CCure Badge\|[^\|]*\|({result}.+?)\|"""
]
ParserVersion = "v1.0.0"


}
```