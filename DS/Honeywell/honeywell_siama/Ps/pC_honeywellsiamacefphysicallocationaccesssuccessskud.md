#### Parser Content
```Java
{
Name = "honeywell-siama-cef-physical-location-access-success-skud"
Vendor = "Honeywell"
Product = "Honeywell siama"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|SKUD|SKUD|"""
  """|SKUD """
  """externalId="""
  """eventId="""
]
Fields = [
  """\Wrt=({time}\d{13})"""
  """\Wahost=({host}[\w\-.]+)"""
  """\Wsuser=({last_name}[^,=]+),\s*({first_name}[^,=]+?)\s+(\w+=|$)"""
  """\Wduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)"""
  """\Wsuid=({user_id}[^\s]+)"""
  """\Wmsg=({location_door}.+?)\s+(\w+=|$)"""
  """\Wcn2=({src_location_id}.+?)\s+(\w+=|$)"""
  """\Wcn3=({location_door_id}.+?)\s+(\w+=|$)"""
  """\Wcn1=({door_side_id}.+?)\s+(\w+=|$)"""
  """CEF:([^\|]*\|){5}({event_name}[^\|]+)"""
]
DupFields = [
  """user_id->badge_id"""
]
ParserVersion = "v1.0.0"


}
```