#### Parser Content
```Java
{
Name = "tyco-ccure-cef-physical-location-access-fail-flexnumber"
Vendor = "Tyco"
Product = "CCURE Building Management System"
TimeFormat = "epoch"
Conditions = ["""CEF:""", """|CCURE|ACS|""", """flexNumber1="""]
Fields = [
"""\sdvc=({host}[^\s]+)"""
"""\sdvchost=({host}[^\s]+)"""
"""(?:([^\|]*\|)){5}({result}[^\|]+)"""
"""\srt=({time}\d{13})"""
"""\ssuser=(?:N\/A|({user}.+?))\s(\w+=|$)"""
"""\scs1=({first_name}.+?)\s(\w+=|$)"""
"""\scs2=({last_name}.+?)\s(\w+=|$)"""
"""\sflexNumber1=({badge_id}\d+)"""
"""\scs4=({department}.+?)\s(\w+=|$)"""
"""\scs5=({company}.+?)\s(\w+=|$)"""
"""\smsg=({location_door}.+?)\s(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```