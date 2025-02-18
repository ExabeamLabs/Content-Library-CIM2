#### Parser Content
```Java
{
Name = microsoft-evsetup-xml-app-activity-setup-1
  Product = Event Viewer - Setup  
  Conditions = [ """<Provider Name ='Microsoft-Windows-WUSA'""", """<Channel>Setup</Channel>""", """<EventID>""", """<Computer>""" ]
  ParserVersion = "v1.0.0"
  Fields = ${WindowsParsersTemplates.windows-xml-events.Fields}[
    """<Data Name ='UpdateTitle'>"({event_name}[^"<]+)"""
    """<Data Name ='ErrorCode'>({failure_code}[^<]+)<""",   
    """<Data Name ='CommandLine'>({process_command_line}.+?)\s*</Data>"""    
  ]

windows-xml-events = {
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