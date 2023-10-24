#### Parser Content
```Java
{
Name = "honeywell-pw-json-physical-location-access-areaname"
Vendor = "Honeywell"
Product = "Honeywell Pro-Watch"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """"fielddatetime":""""
  """"areaname":""""
  """"cardholderid":"""
  """"locationfullname":""""
  """"cardholderfirstname":""""
]
Fields = [
  """"fielddatetime\":\"({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
  """"source\":\"({src_host}[\w\-.]+)"""
  """"category\":({category}\d+)"""
  """"eventid\":({event_code}\d+)"""
  """"cardholderid\":({badge_id}\d+)"""
  """"areacode\":({area_code}\d+)"""
  """"description\":\"({additional_info}[^\"]+)"""
  """"accessreason\":\"({action}[^\"]+)"""
  """"locationfullname\":\"({location_full}[^\"]+)"""
  """"areaname\":\"({location_area}[^\"]+)"""
  """"cardnumber\":\"({card_num}[^\"]+)"""
  """"cardholderfirstname\":\"({first_name}[^\"]+)"""
  """"cardholderlastname\":\"({last_name}[^\"]+)"""
  """"zoneentered\":\"({location_door}[^\"]+)"""
]
DupFields = [
  "location_area->location_building"
]
ParserVersion = "v1.0.0"


}
```