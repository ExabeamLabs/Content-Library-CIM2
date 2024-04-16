#### Parser Content
```Java
{
Name = "badge-b-csv-physical-location-access-fail-nozoneprivilege"
Vendor = "Badge"
Product = "Badge"
TimeFormat = ["dd/MM/yyyy HH:mm:ss a","dd/M/yyyy HH:mm:ss a"]
Conditions = [
""""Access Denied""""
"""No Zone Privilege"""
]
Fields = [
"""({time}\d+\/\d+\/\d\d\d\d\s+\d+:\d+:\d+\s+(AM|PM|am|pm)),"({action}Access Denied)","({result_reason}[^"]+)","({full_name}[^",\s]+\s+[^,]+),\s*({user}[\w\.\-]{1,40}\$?)\s+was denied access into (Access Zone )?({location_door}[^"]+?)\s+(({direction}IN|OUT)\s+)?through"""
"""({time}\d+\/\d+\/\d\d\d\d\s+\d+:\d+:\d+\s+(AM|PM|am|pm)),"({action}Access Denied)","({result_reason}[^"]+)","(CSL Vendor|({user}[\w\.\-]{1,40}\$?)),\s*({full_name}[^"\)]+?)\s+was denied access into (Access Zone )?({location_door}[^"]+?)\s+(({direction}IN|OUT)\s+)?through"""
""""Card number\s*\(({badge_id}[^\s\)]+)"""
]
DupFields = [
"action->event_name"
]
ParserVersion = "v1.0.0"


}
```