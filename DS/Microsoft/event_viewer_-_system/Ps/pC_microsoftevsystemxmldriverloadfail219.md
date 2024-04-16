#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-driver-load-fail-219
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>219</EventID>""", """<TimeCreated SystemTime""" ]
  Fields = ${WindowsParsersTemplates.s-xml-object-access-1.Fields}[
    """<EventID>({event_code}219)""",
  ]

s-xml-object-access-1 = {
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({dest_host}({host}[\w\-.]+?))<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Message>({event_name}[^.<]+?)\s*<\/Message>""",
    """<Message>({event_name}[^<]+?)\s*\.(\s|<\/Message>)""",
    """<EventID Qualifiers\\*='\d+'>({event_code}\d+)<\/EventID>""",
    """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>""",
    """<Keywords?>({result}[^<]+)<\/Keywords?>""",
    """<Security UserID\\*='({user_sid}[^']+)""",
    """User SID:\s*({user_sid}[^\s]+)""",
    """User Name:\s*({user}[\w\.\-]{1,40}\$?)""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
    """<Execution ProcessID\\*='({process_id}[^']+)""",
    """<Provider>({provider_name}[^<]+?)</Provider>""",
    """ThreadID\\*='({thread_id}[^']+)""",
    """File Name:\s*({file_path}({file_dir}(?:[^<]+)?[\\\/])?({file_name}[^\\\/<]+?(\.({file_ext}[^\\\/\.<\s]+?))))\s+\w+:""",
    """Hash:\s*((&lt;None&gt;)|({file_hash}[^\s]+))""",
    """<Level>({run_level}[^<]+)<"""
  
}
```