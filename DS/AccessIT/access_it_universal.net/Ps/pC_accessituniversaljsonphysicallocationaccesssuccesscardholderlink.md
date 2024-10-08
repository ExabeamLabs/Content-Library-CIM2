#### Parser Content
```Java
{
Name = "accessit-universal-json-physical-location-access-success-cardholderlink"
Vendor = "AccessIT"
Product = "Access IT Universal.NET"
TimeFormat = "yyyy.MM.dd.HH.mm.ss"
Conditions = [
""""globallyuniqueeventid":"""
""""cardholderlink":"""
]
Fields = [
""""globallyuniqueeventid":"({time}\d\d\d\d.\d\d.\d\d.\d\d.\d\d.\d\d)"""
""""cardnumber":({badge_id}\d+)"""
""""accountname":"({user}[\w\.\-]{1,40}\$?)"""
""""cardholder":"({last_name}[^,]+),\s({first_name}[^"]+)"""
""""eventlocation":"({location_door}[^"]+)"""
""""eventdescription":"({action}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```