#### Parser Content
```Java
{
Name = "accessit-universal-json-physical-location-access-success-cardholderlink"
Vendor = "AccessIT"
Product = "AccessIT Universal.NET"
TimeFormat = [ "yyyy.MM.dd.HH.mm.ss" , "yyyy.MM.dd.HH.mm.ss.SSSSSSS" ]
ExtractionType = json
Conditions = [
""""globallyuniqueeventid":"""
""""cardholderlink":"""
]
Fields = [
"""exa_json_path=$.globallyuniqueeventid,exa_field_name=time""",
"""exa_json_path=$.cardnumber,exa_field_name=badge_id""",
"""exa_json_path=$.accountname,exa_regex=({user}[\w\.\-]{1,40}\$?)""",
"""exa_json_path=$.cardholder,exa_regex=({last_name}[^,]+),\s({first_name}[^"]+)""",
"""exa_json_path=$.eventlocation,exa_field_name=location_door""",
"""exa_json_path=$.eventdescription,exa_field_name=action""",
]
ParserVersion = "v1.0.0"


}
```