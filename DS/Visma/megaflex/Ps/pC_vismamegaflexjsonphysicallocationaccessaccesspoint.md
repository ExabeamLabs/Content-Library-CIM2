#### Parser Content
```Java
{
Name = visma-megaflex-json-physical-location-access-accesspoint
  Vendor = Visma
  Product = Megaflex
  TimeFormat = "epoch"
  Conditions = [ """"decision":"""", """accessPoint""" ]
  Fields = [
    """"decision":"({result}[^"]+)"""",
    """"eventTime":({time}\d{13}),""",
    """"person".*?"id":({user_id}\d+)""",
    """"firstName":"({first_name}[^"]+)"""",
    """"lastName":"({last_name}[^"]+)"""",
    """"token".*?"id":({badge_id}\d+)""",
    """"destinationArea".*?"type":"({location_area}[^"]+)"""",
    """"destinationArea".*?"id":({location_door_id}[^,]+),""",
    """"destinationArea".*?"name":"({location_full}[^"]+)"""",
    """"sourceArea".*?"type":"({source_location_area}[^"]+)"""",
    """"sourceArea".*?"id":({source_location_door_id}[^,]+),""",
    """"sourceArea".*?"name":"({source_location_full}[^"]+)"""",
  ]
  ParserVersion = "v1.0.0"


}
```