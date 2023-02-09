#### Parser Content
```Java
{
Name = microsoft-evapp-xml-process-create-100
  ParserVersion = "v1.0.0"
  Product = Event Viewer - Application
  Conditions = [ """<EventID Qualifiers='""", """'>100</EventID>""", """<TimeCreated SystemTime=""" ]

s-xml-object-access-1 = {
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Fields = [
    """<TimeCreated SystemTime='({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({host}[^<>]+?)<\/Computer>""",
    """<Message>({event_name}[^.<]+?)\s*<\/Message>""",
    """<Message>({event_name}[^<]+?)\s*\.(\s|<\/Message>)""",
    """<EventID Qualifiers='\d+'>({event_code}\d+)<\/EventID>""",
    """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>""",
    """<Keywords?>({result}[^<]+)<\/Keywords?>""",
    """<Security UserID='({user_sid}[^']+)""",
    """User SID:\s*({user_sid}[^\s]+)""",
    """User Name:\s*({user}[^\s]+)""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
    """<Execution ProcessID='({process_id}[^']+)""",
    """<Provider>({provider_name}[^<]+?)</Provider>""",
    """ThreadID='({thread_id}[^']+)""",
    """File Name:\s*({file_path}({file_dir}(?:[^<]+)?[\\\/])?({file_name}[^\\\/<]+?(\.({file_ext}[^\\\/\.<\s]+?))))\s+\w+:""",
    """Hash:\s*((&lt;None&gt;)|({file_hash}[^\s]+))""",
  ]
  DupFields = [ "host->dest_host" 
}
```