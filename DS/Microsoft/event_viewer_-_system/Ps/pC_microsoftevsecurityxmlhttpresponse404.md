#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-http-response-404
  Product = Event Viewer - System
  ParserVersion = v1.0.0
  Conditions = [ """>404</EventID>""", """<TimeCreated SystemTime""","""<Channel>System</Channel>""" ]
  Fields = ${DLWindowsParsersTemplates.s-xml-events.Fields}[
    """<Computer>({host}[\w\-.]+?)<""",
    """Status Code:\s*({http_response_code}\d+)""",
    """<EventData><Data>({instance_id}[^<]+)"""
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w\-\.]+)"""
     ]

s-xml-events = {
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[\w\.\-]+)<""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{9}Z)"""
    """>({event_code}\d+)</EventID>""",
    """<Security UserID=('|")({user_sid}[^'"]+)('|")\/>""",
    """<Execution ProcessID=('|")({process_id}\d+)('|") ThreadID=('|")({thread_id}\d+)('|")\/>""",
    """<Level>({run_level}[^<]+)<""",
    """<Provider Name =('|")({provider_name}[^'"]+)('|")""",
    """Guid=('|")\{({process_guid}[^\}'"]+?)\}('|")""",
    """<Task>({task_name}[^<]+)""",
    """<Opcode>(0|({opcode}[^<]+))<""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<EventRecordID>({event_id}[^<]+)""",
    """<Channel>({channel}[^<]+)<"""
  
}
```