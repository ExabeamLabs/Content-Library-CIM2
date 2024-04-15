#### Parser Content
```Java
{
Name = "galaxy-g-kv-physical-location-access-accessinfo"
Vendor = "Galaxy"
Product = "Galaxy"
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
""", LAN_ID = """
""", READER_NAME = """
""", Access_Info = """
]
Fields = [
"""Date_tiem\s*=\s*({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)"""
"""LAN_ID\s*=\s*({user}[^\s,]+)"""
"""READER_NAME\s*=\s*({location_door}[^,]+)"""
"""OFFICE\s*=\s*({location_building}.+?)\s+({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}).+?, ([\w\s]+=|$)"""
"""Access_Info\s*=\s*({action}[^,]+?)[\s,]*([\w\s]+=|$)"""
]
ParserVersion = "v1.0.0"


}
```