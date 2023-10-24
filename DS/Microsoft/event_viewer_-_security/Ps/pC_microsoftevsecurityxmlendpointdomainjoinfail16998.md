#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-domain-join-fail-16998"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = ["""<Event xmlns=""",""">16998</EventID>""","""<EventRecordID>"""]
Fields = [
  """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z'\/>"""
  """<Computer>({dest_host}({host}[^<]+))</Computer>"""
  """EventData Name ='({event_name}[^>']+)"""
  """({event_code}\d+)<\/EventID>"""
  """<Keywords>({result}[^<]+)"""
  """<EventRecordID>({event_id}[^<]+)"""
  """<Execution ProcessID='({process_id}\d+)' ThreadID='({thread_id}\d+)'\/>"""
  """<Security UserID='({user_sid}[^']+)'\/>""",
  """<Data Name ='Computer Account SID:'>({dest_user_sid}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```