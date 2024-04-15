#### Parser Content
```Java
{
Name = "badge-b-kv-physical-location-access-personname"
Vendor = "Badge"
Product = "Badge"
TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
Conditions = [
  """, ID=""""
  """, PersonName =""""
  """, DoorName =""""
  """, CardNumber=""""
]
Fields = [
  """\sController="({host}[^\"]+)"""
  """\sTimeStamp="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d)"""
  """\sID=\"({employee_id}[^\"]+)"""
  """\sPersonName ="({last_name}[^\"_]+?)\s*_({first_name}[^\"_]+?)\s*(_({middle_initial}[^\"_\s]+?))?\s*\""""
  """\sAreaName ="({location_building}[^\"]+?)(_({direction}In|Out))?\""""
  """\sDoorName ="({location_door}[^\"]+)"""
  """\sCardNumber="({badge_id}\d+)"""
  """\sEventType="({action}[^\"]+)"""
]
ParserVersion = "v1.0.0"


}
```