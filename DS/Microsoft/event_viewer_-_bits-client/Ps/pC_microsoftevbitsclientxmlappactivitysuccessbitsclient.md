#### Parser Content
```Java
{
Name = microsoft-evbitsclient-xml-app-activity-success-bitsclient
  ExtractionType = regex
  Vendor = Microsoft
  Product = Event Viewer - BITS-Client
  ParserVersion = v1.0.0
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSS" ]
  Conditions = [ "<Channel>Microsoft-Windows-Bits-Client/Operational<", "<EventID>59<", "Microsoft-Windows-Bits-Client" ]
  Fields = [ 
    """<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Security UserID(\\)?=('|")({user_sid}[^'"]+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}[^'"]+)""",
    """<EventID>({event_code}59)""", 
    """ThreadID(\\)?=('|")({thread_id}\d+)""",
    """<Level>({run_level}[^<]+)<""",
    """<Computer>({src_host}({host}[^<]+?))<""",
    """<Channel>({channel}[^<]+)<""",
    """<Data\s*Name =["']url["']>({url}[^<]+)<""",
    """<Data\s*Name =["']name["']>({event_name}[^<\{]+)[<\{]"""
	]


}
```