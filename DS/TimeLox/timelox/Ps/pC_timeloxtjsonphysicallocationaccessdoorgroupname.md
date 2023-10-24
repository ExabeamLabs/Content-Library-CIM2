#### Parser Content
```Java
{
Name = "timelox-t-json-physical-location-access-doorgroupname"
Vendor = "TimeLox"
Product = "TimeLox"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"eventtime":""""
  """"doorgroupname":""""
  """"issued by":"""
]
Fields = [
  """"doorgroupname\":\"({door_group_name}[^\"]+)"""
  """"eventtime\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  """"registration no\.\":({registration_no}\d+)"""
  """"userid\":\"({user_id}[^\"]+)"""
  """"event\":\"({action}[^\"]+)"""
  """"issued by\":\"(n\/a|({user}[\w\.\-]{1,40}\$?))"""
  """"door\":\"({location_door}[^\"]+)"""
  """"blockinggroupname\":\"(n\/a|({blocking_group_name}[^\"]+))"""
  """"@version\":\"({version}[^\"]+)"""
  """"user group\":\"({user_group_name}[^\"]+)"""
]
ParserVersion = "v1.0.0"


}
```