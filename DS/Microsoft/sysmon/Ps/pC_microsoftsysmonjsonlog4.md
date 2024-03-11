#### Parser Content
```Java
{
Name = microsoft-sysmon-json-log-4
  Vendor = Microsoft
  Product = Sysmon
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """"EventID":4,""", """"Hostname":""", """"State":""", """"RecordNumber":""" ]
  Fields = [
    """UtcTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """Hostname":"({host}[^"]+)""",
    """Domain":"((?i)(NT AUTHORITY)|({domain}[^"]+))""",
    """EventID":({event_code}4),""",
    """({event_name}Sysmon service state changed)""",
    """RecordNumber":({event_id}\d+)""",
    """"Keywords":({result}[^,]+)""",
    """UserID":"({user_sid}[^"]+)""",
    """State":"({state}[^"]+)""",
    """ProcessID":({process_id}\d+)""",
    """AccountName":"((?i)SYSTEM|({user}[^"]+))""",
    """State":"({state}[^"]+)""",
    """"AccountName":"((?i)system|({user}[^"]+))"""",
    """"({log_name}Microsoft-Windows-Sysmon)"""
  ]


}
```