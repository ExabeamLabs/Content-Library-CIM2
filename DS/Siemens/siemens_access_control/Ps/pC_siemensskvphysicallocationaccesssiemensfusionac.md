#### Parser Content
```Java
{
Name = "siemens-s-kv-physical-location-access-siemensfusionac"
Vendor = "Siemens"
Product = "Siemens Access Control"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""%SIEMENS_FUSION_AC:"""
]
Fields = [
"""%SIEMENS_FUSION_AC:(.+?(\^){2}){1}({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""%SIEMENS_FUSION_AC:(.+?(\^){2}){4}({employee_id}(NE-)?\d+)"""
"""%SIEMENS_FUSION_AC:(.+?(\^){2}){6}({badge_id}\d+)"""
"""%SIEMENS_FUSION_AC:(.+?(\^){2}){8}({action}.+?)(\^)+"""
"""%SIEMENS_FUSION_AC:(.+?(\^){2}){10}({location_door}.+?)(\^)+"""
"""%SIEMENS_FUSION_AC:(.+?(\^){2}){12}({location_building}.+?)(\^)+"""
"""%SIEMENS_FUSION_AC:(.+?(\^){2}){14}({location_city}.+?)(\^)+"""
]
ParserVersion = "v1.0.0"


}
```