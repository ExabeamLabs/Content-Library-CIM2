#### Parser Content
```Java
{
Name = "honeywell-pw-csv-physical-location-access-success-exabeam"
Vendor = "Honeywell"
Product = "Honeywell Pro-Watch"
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
  """prowatch:exabeam"""
  """ExaBeamTransaction"""
]
Fields = [
  """({employee_id}\w*)\|({first_name}[^|]*)\|({last_name}[^|]*)\|(\s*|({location_building}[^|]*))\|({location_city}[^|]*)\|(\s*|({location_state}[^|]*))\|({department}[^|]*)\|({badge_id}[^|]*)\|({location_door}.*?)\s*\|({time}\d\d\/\d\d\/\d{4} \d\d:\d\d:\d\d)\|({result}[^"]*)"""
]
ParserVersion = "v1.0.0"


}
```