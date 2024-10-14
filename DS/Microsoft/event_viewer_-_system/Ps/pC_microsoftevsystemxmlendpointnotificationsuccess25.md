#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-endpoint-notification-success-25
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<Provider Name""", """<EventID>25</EventID>""", """<Provider Name =""", """Microsoft-Windows-Kernel-Boot""", """BootMenuPolicy""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{1,9}Z)""",
    """<Computer>({dest_host}({host}[\w\-.]+))""",
    """<EventID>({event_code}25)""",
    """ProcessID\\*=('|"")({process_id}\d+)'""",
    """ThreadID\\*=('|")({thread_id}\d+)'""",
    """<Security UserID\\*='({user_sid}[^']+)'""",
    """Guid\\*='\{({process_guid}[^'}]+)"""
    """<Data Name =('|")({event_name}[^"]+)"""
    """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>""",
    """<Provider>({provider_name}[^<]+?)</Provider>""",
    """ThreadID\\*='({thread_id}[^']+)""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<Level>({run_level}[^<]+)<"""
  ]


}
```