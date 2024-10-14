#### Parser Content
```Java
{
Name = microsoft-evwinfirewall-xml-endpoint-activity-success-winfirewall
  ExtractionType = regex
  Vendor = Microsoft
  Product = Event Viewer - Windows Firewall
  ParserVersion = v1.0.0
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SS", "yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSS" ]
  Conditions = [ "<Channel>Microsoft-Windows-Windows Firewall With Advanced Security/Firewall<", "Microsoft-Windows-Windows Firewall With Advanced Security", "<EventID>", "<Computer>" ]
  Fields = [ 
    """<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<EventID>({event_code}\d+)<""",
    """<Computer>({host}[^<>]+)<""",
    """<Level>({run_level}[^<]+)<""",
    """<Channel>({channel}[^<]+)<""",
    """<Security UserID(\\)?=('|")({user_sid}[^'"]+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}[^'"]+)""",
    """ThreadID(\\)?=('|")({thread_id}\d+)""",
	]


}
```