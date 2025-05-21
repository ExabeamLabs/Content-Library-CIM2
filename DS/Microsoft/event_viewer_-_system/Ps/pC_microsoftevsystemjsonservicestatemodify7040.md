#### Parser Content
```Java
{
Name = microsoft-evsystem-json-service-state-modify-7040
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"SourceName":"Service Control Manager"""", """"EventID":""", """7040""", """The start type of""", """service was changed from""" ]
  Fields = [
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"Hostname":"({host}[^"]+)"""",
    """"EventID":({event_code}\d+)""",
    """"SourceName":"({log_source}[^"]+)"""",
    """"ProviderGuid":"({process_guid}[^"]+)"""",
    """"ProcessID":({process_id}\d+)""",
    """"Channel":"({channel}[^"]+)"""",
    """"Domain":"((?i)NT AUTHORITY|NT-AUTORIT|({domain}[^"\\]+))""",
    """"AccountName":"((?i)system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"UserID":"({user_sid}[^"]+)"""",
    """"AccountType":"({user_type}[^"]+)"""",
    """"Message":"({additional_info}[^,]+)"""",
    """"param2":"({old_value}[^"]+?)"""",
    """"param3":"({new_value}[^"]+?)"""",
  ]


}
```