#### Parser Content
```Java
{
Name = "brivo-b-json-physical-location-access-sitename"
Vendor = "Brivo"
Product = "Brivo"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""occurred":"""
""""siteName":"""
]
Fields = [
""""occurred":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d+)Z)"""
""""siteName":\s*"\s*({location_building}[^"]+?)\s*""""
""""objectName":\s*"\s*({location_door}[^"]+?)\s*""""
""""firstName":\s*"({first_name}[^"]+)"""
""""lastName":\s*"({last_name}[^"]+)"""
""""description":\s*"({action}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```