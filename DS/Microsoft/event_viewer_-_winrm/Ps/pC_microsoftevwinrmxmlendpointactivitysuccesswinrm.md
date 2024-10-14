#### Parser Content
```Java
{
Name = microsoft-evwinrm-xml-endpoint-activity-success-winrm
  ExtractionType = regex
  Vendor = Microsoft
  Product = Event Viewer - WinRM
  ParserVersion = v1.0.0
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SS", "yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSS" ]
  Conditions = [ "<Channel>Microsoft-Windows-WinRM/Operational<", "Microsoft-Windows-WinRM", "<Computer>", "<EventID>" ]
  Fields = [ 
    """<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<EventID>({event_code}\d+)<""",
    """<Computer>({host}[^<>]+)<""",
    """<Level>({run_level}[^<]+)<""",
    """<Channel>({channel}[^<]+)<""",
    """<Security UserID(\\)?=('|")({user_sid}[^'"]+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}[^'"]+)""",
    """ThreadID(\\)?=('|")({thread_id}\d+)""",
    """<ErrorCode>({error_code}\d+)<"""
	]


}
```