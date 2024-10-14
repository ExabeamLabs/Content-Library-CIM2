#### Parser Content
```Java
{
Name = microsoft-evkernelpnp-xml-endpoint-activity-success-kernelpnp
  ExtractionType = regex
  Vendor = Microsoft
  Product = Event Viewer - Kernel-PnP
  ParserVersion = v1.0.0
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SS", "yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSS" ]
  Conditions = [ "<Channel>Microsoft-Windows-Kernel-PnP/Configuration<", "<EventID>", "Microsoft-Windows-Kernel-PnP", "<Computer>" ]
  Fields = [ 
    """<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<EventID>({event_code}\d+)<""",
    """<Computer>({host}[^<>]+)<""",
    """<Level>({run_level}[^<]+)<""", 
    """<Channel>({channel}[^<]+)<""",
    """<Security UserID(\\)?=('|")({user_sid}[^'"]+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}[^'"]+)""",
    """ThreadID(\\)?=('|")({thread_id}\d+)""",
    """<Data\s*Name =["']DriverName["']>({driver_name}[^<]+)<""",
    """<Data\s*Name =["']Status["']>({execution_status}[^<]+)<""",
    """<Data\s*Name =["']DriverVersion["']>({version}[^<]+)<"""
	]


}
```