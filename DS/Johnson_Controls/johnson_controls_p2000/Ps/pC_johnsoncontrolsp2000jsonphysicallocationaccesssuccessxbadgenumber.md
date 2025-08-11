#### Parser Content
```Java
{
Name = "johnsoncontrols-p2000-json-physical-location-access-success-xbadgenumber"
ExtractionType = json
Vendor = "Johnson Controls"
Product = "Johnson Controls P2000"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"x_badge_number""""
  """"x_fac_code""""
  """"x_timed_overrd""""
  """"x_cardholder_guid""""
  """"x_cardholder_nick_name""""
]
Fields = [
  """exa_json_path=$.x_timestamp,exa_field_name=time""",
  """exa_json_path=$.x_badge_number,exa_field_name=badge_id""",
  """exa_json_path=$.x_fname,exa_field_name=first_name""",
  """exa_json_path=$.x_lname,exa_field_name=last_name""",
  """exa_json_path=$.x_event_name,exa_field_name=event_name""",
  """exa_json_path=$.x_panel_name,exa_field_name=location_building""",
  """exa_json_path=$.x_term_name,exa_field_name=location_door""",
  """exa_json_path=$.x_item_name,exa_field_name=additional_info""",
  """exa_json_path=$.site,exa_field_name=location_city""",
]
ParserVersion = "v1.0.0"


}
```