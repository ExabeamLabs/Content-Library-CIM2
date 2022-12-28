#### Parser Content
```Java
{
Name = badge-b-kv-physical-location-access-accessevent
 Vendor = Badge
 Product = Badge
 TimeFormat = "yyyy-MM-dd HH:mm:ss"
 Conditions = [ """Badge_ID""", """Access_Event""", """Reader_Description"""]
 Fields = [
   """Badge_ID=({badge_id}\d+)""",
   """First_Name ="+({first_name}[^"]+)""",
   """Last_Name ="+({last_name}[^"]+)""",
   """Access_Event="+({result}[^"]+)""",
   """Reader_Description="+({location_building}[^-\s]+)""",
   """Reader_Description="+({location_door}[^"]+)""",
   """Location="+({location_city}[^"]+)"""
 ]
 ParserVersion = "v1.0.0"


}
```