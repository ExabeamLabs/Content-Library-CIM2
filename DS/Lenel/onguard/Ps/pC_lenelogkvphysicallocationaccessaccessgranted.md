#### Parser Content
```Java
{
Name = lenel-og-kv-physical-location-access-accessgranted
    Vendor = Lenel
    Product = OnGuard
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = ["""LOG_TIME_UTC=""","""EVENT_TIME_CT=""", """EVDESCR=""", """READERDESC=""", """MACHINE_NAME=""", """BUILDING_CODE="""]
    Fields = [
      """LOG_TIME_UTC=\\?"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """LOG_HOST=\\?"({host}[^\\"]+)""",
      """CARDNUM="*({badge_id}[^=]+)\s\w+=""",
      """USER=\\?"({user}[\w\.\-]{1,40}\$?)""",
      """EVDESCR=\\?"({result}[^\\"]+)""",
      """LASTNAME=\\?"({last_name}[^\\"]+)""",
      """FIRSTNAME=\\?"({first_name}[^\\"]*?)\s*\\""",
      """READERDESC=\\?"({location_door}[^\\"]+)""",
      """CITY_CODE=\\?"({location_city}[^\\"]+)""",
      """BUILDING_CODE=\\?"({location_building}[^\\"]+)"""
    ]
    ParserVersion = "v1.0.0"
  

}
```