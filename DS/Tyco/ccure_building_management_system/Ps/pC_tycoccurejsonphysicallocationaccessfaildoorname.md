#### Parser Content
```Java
{
Name = "tyco-ccure-json-physical-location-access-fail-doorname"
Vendor = "Tyco"
Product = "CCURE Building Management System"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""ntid":""""
""""personType":""""
""""doorName":""""
]
Fields = [
""""serverName":\s*\"({host}[^\"]+)""""
""""firstName":\s*\"({first_name}[^\"]+)""""
""""lastName":\s*\"({last_name}[^\"]+)""""
""""ntid":\s*\"({user}[^\"]+)""""
""""doorName":\s*\"({location_door}[^\"]+?)\s*""""
""""direction":\s*\"({direction}[^\"]+)""""
""""messageDateTime":\s*\"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
""""admitReject":\s*\"({result}[^\"]+)""""
]
DupFields = [
"location_door->location_full"
]
ParserVersion = "v1.0.0"


}
```