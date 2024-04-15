#### Parser Content
```Java
{
Name = "honeywell-pw-kv-physical-location-access-success-location"
Vendor = "Honeywell"
Product = "Honeywell Pro-Watch"
TimeFormat = "yyyy-MM-dd H:mm:ss"
Conditions = [
  """ EVNT_DESCRP:"""
  """ LOCATION:"""
  """ LNAME:"""
  """ FNAME:"""
]
Fields = [
  """\sEVNT_DAT:\s*"({time}\d\d\d\d-\d\d-\d\d\s+\d{1,2}:\d\d:\d\d)"""
  """\sEVNT_DESCRP:\s*"({result}[^"].*?)"\s*(\w+:|$)"""
  """\sFNAME:\s*"({first_name}[^"].*?)"\s*(\w+:|$)"""
  """\sLNAME:\s*"({last_name}[^"].*?)"\s*(\w+:|$)"""
  """\sLOCATION:\s*"({location_door}[^"].*?)"\s*(\w+:|$)"""
  """\sLOOP_DESCRP:\s*"({location_building}[^"].*?)"\s*(\w+:|$)"""
  """\sCARDNO:\s*"({badge_id}[^"].*?)"\s*(\w+:|$)"""
]
ParserVersion = "v1.0.0"


}
```