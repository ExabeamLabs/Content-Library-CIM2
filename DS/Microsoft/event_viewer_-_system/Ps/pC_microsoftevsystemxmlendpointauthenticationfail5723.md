#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-endpoint-authentication-fail-5723
  ParserVersion = "v1.0.0"
  Product = Event Viewer - System
  Conditions = [ """>5723</EventID>""", """<TimeCreated SystemTime""" ]
  Fields = ${DLWindowsParsersTemplates.s-xml-events.Fields}[
    """<Computer>({host}[\w\-.]+?)<""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  ]
  DupFields = ["additional_info->failure_reason"]

s-xml-events = {
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[\w\.\-]+)<""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{9}Z)"""
    """>({event_code}\d+)</EventID>""",
    """<Security UserID='({user_sid}[^']+)'\/>""",
    """<Execution ProcessID='({process_id}\d+)' ThreadID='({thread_id}\d+)'\/>""",
    """<Level>({run_level}[^<]+)<""",
    """<Provider Name ='({provider_name}[^']+)'""",
    """Guid='\{({process_guid}[^}]+?)\}""",
    """<Task>({task_name}[^<]+)""",
    """<Opcode>(0|({opcode}[^<]+))<""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<EventRecordID>({event_id}[^<]+)""",
    """<Channel>({channel}[^<]+)<"""
  
}
```