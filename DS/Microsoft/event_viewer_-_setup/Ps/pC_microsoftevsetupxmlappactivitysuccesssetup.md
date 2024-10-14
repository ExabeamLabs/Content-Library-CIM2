#### Parser Content
```Java
{
Name = microsoft-evsetup-xml-app-activity-success-setup
  ExtractionType = regex
  Vendor = Microsoft
  Product = Event Viewer - Setup
  ParserVersion = v1.0.0
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSS" ]
  Conditions = [ "<Channel>Setup<", "<EventID>", "Microsoft-Windows-Servicing" ]
  Fields = [ 
    """<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Security UserID(\\)?=('|")({user_sid}[^'"]+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}[^'"]+)""",
    """<EventID>({event_code}\d+)<""",
    """ThreadID(\\)?=('|")({thread_id}\d+)""",
    """<Level>({run_level}[^<]+)<""",
    """<Computer>({src_host}({host}[^<>]+))<""",
    """<Channel>({channel}[^<]+)<""",
    """<PackageIdentifier>({identifier}[^<]+)<"""
	]


}
```