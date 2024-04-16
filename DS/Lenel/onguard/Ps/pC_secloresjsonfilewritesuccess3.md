#### Parser Content
```Java
{
Name = seclore-s-json-file-write-success-3
ExtractionType = json
Conditions = [
  """"machine_name""""
  """"activity":"""
  """"user_name":"""
  """"offline_access_right":"""
  """"activity":3"""
]
ParserVersion = "v1.0.0"

lenel-physical-access = {
    Vendor = Lenel
    Product = OnGuard
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
    Fields = [
       """"CARDNUM":\s*({badge_id}\d+)""",
       """"FIRSTNAME":\s*"({first_name}[^"]+?)\s*"""",
       """"Hostname":\s*"({host}[^"]+)""",
       """"LASTNAME":\s*"({last_name}[^"]+?)\s*"""",
       """"READERDESC":\s*"({location_door}[^"]+)""",
       """"EVTDESCR":\s*"({result}[^"]+)""",
       """"EVENT_TIME_UTC":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6})""",
       """"EMPID":\s*"({employee_id}[^"]+?)\s*""""
    ]
    DupFields = [ "location_door->location_full" 
}
```