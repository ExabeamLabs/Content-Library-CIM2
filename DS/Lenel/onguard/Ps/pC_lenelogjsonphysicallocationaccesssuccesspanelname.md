#### Parser Content
```Java
{
Name = "lenel-og-json-physical-location-access-success-panelname"
Vendor = "Lenel"
Product = "OnGuard"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
""""readerdesc""""
""""segmentname""""
""""panelname""""
""""badgekey""""
""""event_time_utc""""
""""changedate""""
]
Fields = [
""""host"+:\s*"+({host}[^"]+)""""
""""event_time_utc"+:"+({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d)"""
""""lastname"+:\s*"+({last_name}[^"]+)""""
""""firstname"+:\s*"+({first_name}[^"]+)""""
""""cardnum"+:({card_num}\d+)"""
""""readerdesc"+:\s*"+({location_door}[^"]+)""""
""""devid"+:({devid}\d+)"""
""""panelname"+:\s*"+({location_building}[^"]+)""""
""""emp_id"+:({employee_id}\d+)"""
""""badgekey":({badge_id}\d+)"""
]
ParserVersion = "v1.0.0"


}
```