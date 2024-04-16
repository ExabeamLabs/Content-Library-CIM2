#### Parser Content
```Java
{
Name = lenel-og-kv-physical-location-access-accessgranted
    ExtractionType = json
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
      """exa_json_path=$.message,exa_regex=LOG_TIME_UTC=\\?"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """exa_json_path=$.message,exa_regex=LOG_HOST=\\?"({host}[^\\"]+)""",
      """exa_json_path=$.message,exa_regex=CARDNUM="*({badge_id}[^=]+)\s\w+=""",
      """exa_json_path=$.message,exa_regex=USER=\\?"({user}[\w\.\-]{1,40}\$?)""",
      """exa_json_path=$.message,exa_regex=EVDESCR=\\?"({result}[^\\"]+)""",
      """exa_json_path=$.message,exa_regex=LASTNAME=\\?"({last_name}[^\\"]+)""",
      """exa_json_path=$.message,exa_regex=FIRSTNAME=\\?"({first_name}[^\\"]+)""",
      """exa_json_path=$.message,exa_regex=READERDESC=\\?"({location_door}[^\\"]+)""",
      """exa_json_path=$.message,exa_regex=CITY_CODE=\\?"({location_city}[^\\"]+)""",
      """exa_json_path=$.message,exa_regex=BUILDING_CODE=\\?"({location_building}[^\\"]+)"""
    ]
    ParserVersion = "v1.0.0"
  

}
```