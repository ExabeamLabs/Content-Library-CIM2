#### Parser Content
```Java
{
Name = microsoft-evapp-xml-endpoint-notification-success-1400
  Vendor = Microsoft
  Product = Event Viewer - Application
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>1400</EventID>""", """connector failed to connect to""", """Microsoft-SharePoint Products-SharePoint Server Search""" ]
  Fields = ${DLWindowsParsersTemplates.xml-windows-events-dl.Fields}[
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Message>({event_name}[^<]+)</Message>""",
    """<Data Name\\*='string0'>({additional_info}[^<]+)<""",
    """<Execution ProcessID\\*='({process_id}\d+)' ThreadID\\*='({thread_id}\d+)'\/>""",
    """<Security UserID\\*='({user_sid}[^<']+)"""
  ]

xml-windows-events-dl = {
  Vendor = Microsoft
  Product = Event Viewer - Application
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)('|")""",
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task_name}[^<]+)""",
    """<Execution ProcessID\\*='({process_id}\d+)' ThreadID\\*='({thread_id}\d+)'\/>""",
    """<Security UserID\\*='({user_sid}[^<']+)""",
    """<Data Name\\*=('|")TaskName('|")>({task_name}[^<]+)<"""
    """<Level>({run_level}[^<]+)<""",
    """<Channel>({channel}[^<]+)<\/Channel>"""
  
}
```