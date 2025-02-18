#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-app-notification-500
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """>500</EventID>""", """AD FS Auditing""", """<Channel>Security<""", """Issued identity:""" ]
  Fields = ${DLWindowsParsersTemplates.s-xml-events.Fields}[
    """<Computer>({host}[\w\-.]+?)<""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """Issued identity:.*claims/UPN\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s]+)""",
    """Issued identity:.*/authenticationmethod/({auth_method}[^\s]+)"""
  ]

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