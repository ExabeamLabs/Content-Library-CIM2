#### Parser Content
```Java
{
Name = "gallagher-ac-csv-physical-location-access-noentry"
  Vendor = "Gallagher"
  Product = "Gallagher Access Control"
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """gallagher""", """"No Entry Taken"""" ]
  Fields = [
    """gallagher","({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)","\d*","({result}[^"]+)","({location_door}[^"]+)","({first_name}[^"]+)","({last_name}[^"]+)","({additional_info}[^"]+?\s(to|into)\s({location_building}[^"]+?))\.?(\s*Reason:[^"]*)?","({employee_id}[^"]+)","[^"]*","({badge_id}[^"]+)","({user}[^"]+)"""
  ]
  DupFields = [ "result->event_name" ]


}
```