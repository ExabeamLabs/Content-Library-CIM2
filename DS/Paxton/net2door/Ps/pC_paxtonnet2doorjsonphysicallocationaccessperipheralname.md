#### Parser Content
```Java
{
Name = "paxton-net2door-json-physical-location-access-peripheralname"
Vendor = "Paxton"
Product = "NET2DOOR"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""eventtypedescription""""
""""eventid""""
""""peripheralname""""
]
Fields = [
""""eventtime"*:"*({time}[^"]+)"*(,|$)"""
""""peripheralname"*:"*({location_city}.+?)\s*\-\s*({location_building}.+?)\s*(\(|\-|")"""
""""peripheralname"*:"*([^\-]+)\-([^\-]+)\-\s*(\s*|({location_door}.+?))(\s*\-)?\s*(IN|OUT)"""
""""eventtypedescription"*:"*({action}[^",]+)"*(,|$)"""
""""eventtypedescription"*:"*([^\-]+\-\s*({result_reason}[^",]+))"*(,|$)"""
""""username"*:"*(?:({last_name}[^,]+),\s*({first_name}[^",]+))"*(,|$)"""
""""cardnumber"*:"*({badge_id}\d+)"""
""""userid"*:"*({employee_id}[^",]+)"*(,|$)"""
"""\(({direction}[^\)]+)\)"""
]
ParserVersion = "v1.0.0"


}
```