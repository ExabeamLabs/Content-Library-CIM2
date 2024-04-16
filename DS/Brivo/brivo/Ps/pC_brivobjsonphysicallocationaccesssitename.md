#### Parser Content
```Java
{
Name = "brivo-b-json-physical-location-access-sitename"
Vendor = "Brivo"
Product = "Brivo"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""occurred":"""
""""siteName":"""
]
Fields = [
"""exa_json_path=$.occurred,exa_field_name=time"""
"""exa_json_path=$.siteName,exa_field_name=location_building"""
"""exa_json_path=$.objectName,exa_field_name=location_door"""
"""exa_json_path=$.user.firstName,exa_field_name=first_name"""
"""exa_json_path=$.user.lastName,exa_field_name=last_name"""
"""exa_json_path=$.description,exa_field_name=action"""
]
ParserVersion = "v1.0.0"


}
```