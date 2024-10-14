#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-fail-16977"
Vendor = "Microsoft"
Product = "Event Viewer - System"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = ["""<Event xmlns=""",""">16977</EventID>""","""<EventRecordID>""" , """MinimumPasswordLength""","""<Channel>System</Channel>"""]
Fields = [
  """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z('|")\/>"""
  """<Computer>({dest_host}({host}[^<]+))</Computer>"""
  """EventData Name ='({event_name}[^>']+)"""
  """({event_code}\d+)<\/EventID>"""
  """<Keywords>({result}[^<]+)"""
  """<EventRecordID>({event_id}[^<]+)"""
  """<Execution ProcessID='({process_id}\d+)' ThreadID='({thread_id}\d+)'\/>"""
  """<Security UserID='({user_sid}[^']+)'\/>"""
  """<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```