#### Parser Content
```Java
{
Name = "badge-b-csv-physical-location-access-fail-unauthorisedcard"
Vendor = "Badge"
Product = "Badge"
TimeFormat = ["dd/MM/yyyy HH:mm:ss a","dd/M/yyyy HH:mm:ss a"]
Conditions = [
""""Access Denied""""
""""Unauthorised Card""""
]
Fields = [
"""({time}\d+\/\d+\/\d\d\d\d\s+\d+:\d+:\d+\s+(AM|PM|am|pm)),"({action}Access Denied)","({result_reason}[^"]+)","[^"]+? into\s+(Access Zone\s*)?(\([^\)]*\)\s*)?({location_door}[^"]+?)\s+(({direction}IN|OUT)\s+)?through"""
""""Card number\s*\(({badge_id}[^\s\)]+)"""
]
DupFields = [
"action->event_name"
]
ParserVersion = "v1.0.0"


}
```