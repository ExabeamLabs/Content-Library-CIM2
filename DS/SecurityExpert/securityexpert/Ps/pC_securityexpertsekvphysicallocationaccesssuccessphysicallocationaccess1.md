#### Parser Content
```Java
{
Name = securityexpert-se-kv-physical-location-access-success-physicallocationaccess-1
  Vendor = SecurityExpert
  Product = SecurityExpert
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """UserID="""", """EventID=""", """EventName ="""", """LoggedTime="""" ]
  Fields = [
    """LoggedTime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """DoorName ="({location_door}[^"]+)""",
    """UserID="({badge_id}[^"]+)""",
    """UserName ="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """UserName ="({full_name}[^"\s,]+\s+[^",]+)"""",
    """EventName ="({event_name}[^"]+?)\s*"""",
    """ControllerName ="({device_name}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```