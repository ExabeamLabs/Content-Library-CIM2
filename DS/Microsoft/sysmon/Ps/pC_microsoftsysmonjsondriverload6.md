#### Parser Content
```Java
{
Name = microsoft-sysmon-json-driver-load-6
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"EventID":6,""", """"Hostname":""", """"RecordNumber":""", """"SourceName":"Microsoft-Windows-Sysmon"""" ]
  Fields = [
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """"Hostname":"({dest_host}({host}[^"]+))""",
    """"Domain":"((?i)(NT AUTHORITY)|({domain}[^"]+))""",
    """"EventID":({event_code}6),""",
    """({operation}({event_name}Driver loaded))""",
    """"RecordNumber":({event_id}\d+)""",
    """"Keywords":({result}[^,]+)""",
    """"UserID":"({user_sid}[^"]+)""",
    """"ImageLoaded":"({file_path}(({file_dir}(?:[^"]+)?)[\\\/]+)?({file_name}[^\\\/"]+?(\.({file_ext}[^\\\/\."]+))))""",
    """"Hashes":"MD5=({hash_md5}[^,"]+)""",
    """"AccountName":"((?i)(SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
 ]


}
```