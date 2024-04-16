#### Parser Content
```Java
{
Name = "tyco-ccure-json-physical-location-access-success-user"
Vendor = "Tyco"
Product = "CCURE Building Management System"
TimeFormat = "epoch"
Conditions = [
  """"badge_id":"""
  """"user":"""
  """"location_city":"""
  """"location_building":"""
  """"location_door":"""
  """"location_full":"""
  """"outcome":"""
  """"transaction_time_gmt":"""
  """"direction":"""
]
Fields = [
  """"transaction_time_gmt\":({time}\d{13})"""
  """"user\":\s*\"({user}[\w\.\-]{1,40}\$?)"""
  """"location_door\":({location_door}\d+)"""
  """"location_building\":\s*\"({location_building}[^\"]+)"""
  """"location_city\":\s*\"({location_city}[^\"]+)"""
  """"location_full\":\s*\"({location_full}[^\"]+)"""
  """"outcome\":\s*\"({action}[^\"]+)"""
  """"badge_id\":({badge_id}\d+)"""
  """"direction\":\s*\"({direction}[^\"]+)\""""
]
ParserVersion = "v1.0.0"


}
```