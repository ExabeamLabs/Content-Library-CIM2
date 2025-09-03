#### Parser Content
```Java
{
Name = "rs2-r-str-physical-location-access-lname"
Vendor = "RS2 Technologies"
Product = "RS2 Technologies"
TimeFormat = "yyyy.MM.dd.HH.mm.ss.SSS"
Conditions = [
"""||RS2||"""
]
Fields = [
"""({time}\d\d\d\d\.\d\d\.\d\d\.\d\d\.\d\d\.\d\d\.\d{3})\d*\|\|[^\|]*\|\|(|({full_name}[^\|]+))\|\|([^\|]*\|\|){3}(|({location_full}[^\|]+))\|\|(|({action}[^\|\-]+)(-({failure_reason}[^\|\-]+))?)\|\|(|({badge_id}[^\|]+))\|\|[^\|]*\|\|(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\|\|"""
]
ParserVersion = "v1.0.0"


}
```