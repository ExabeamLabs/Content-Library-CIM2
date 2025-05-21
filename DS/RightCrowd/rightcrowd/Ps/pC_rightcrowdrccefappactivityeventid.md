#### Parser Content
```Java
{
Name = rightcrowd-rc-cef-app-activity-eventid
  Vendor = RightCrowd
  Product = RightCrowd
  TimeFormat =  "epoch"
  Conditions = [ """|RightCrowd|RightCrowd|""","""CEF:""","""eventId=""" ]
  Fields = [
    """ahost=({host}[^\s]+)""",
    """art=({time}\d{13})""",
    """CEF:[^|]+\|([^|]*\|){4}({event_name}[^|]+)""",
    """eventId=({event_code}\d+)""",
    """cn1=({badge_id}\d+)""",
    """cs1=({badge_reader}[^=]+?)\s*\w+=""",
    """categoryOutcome=(\/)?({result}[^\s]+)""",
    """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*\w+=""",
    """suid=({full_name}({last_name}[A-Z][a-z]+)\s*({first_name}\w*))\s+\w+=""",
    """cs5=({site_state}[^\s]+)""",
    """agt=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """cs6=({area_classification}[^=]+)\s+\w+=""",
    """cs4=({site_id}\d+)""",
    """cs3=({site_name}[^=]+)\s+\w+=""",
    """cs2=({badge_status}[^=]+)\s+\w+="""
    ]
    DupFields = [ "badge_reader->location_door" ]
    ParserVersion = "v1.0.0"


}
```