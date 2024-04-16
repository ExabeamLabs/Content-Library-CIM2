#### Parser Content
```Java
{
Name = "honeywell-pw-json-physical-location-access-areaname"
ExtractionType = json
Vendor = "Honeywell"
Product = "Honeywell Pro-Watch"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"fielddatetime":""""
  """"areaname":""""
  """"cardholderid":"""
  """"locationfullname":""""
  """"cardholderfirstname":""""
]
Fields = [
  """exa_json_path=$.fielddatetime,exa_field_name=time""",
  """exa_json_path=$.source,exa_field_name=src_host""",
  """exa_json_path=$.category,exa_field_name=category""",
  """exa_json_path=$.eventid,exa_field_name=event_code""",
  """exa_json_path=$.cardholderid,exa_field_name=badge_id""",
  """exa_json_path=$.areacode,exa_field_name=area_code""",
  """exa_json_path=$.description,exa_field_name=additional_info""",
  """exa_json_path=$.accessreason,exa_field_name=action""",
  """exa_json_path=$.locationfullname,exa_field_name=location_full""",
  """exa_json_path=$.areaname,exa_field_name=location_area""",
  """exa_json_path=$.cardnumber,exa_field_name=card_num""",
  """exa_json_path=$.cardholderfirstname,exa_field_name=first_name""",
  """exa_json_path=$.cardholderlastname,exa_field_name=last_name""",
  """exa_json_path=$.zoneentered,exa_field_name=location_door""",
]
DupFields = [
  "location_area->location_building"
]
ParserVersion = "v1.0.0"


}
```