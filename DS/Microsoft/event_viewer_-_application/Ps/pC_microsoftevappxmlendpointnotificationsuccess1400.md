#### Parser Content
```Java
{
Name = microsoft-evapp-xml-endpoint-notification-success-1400
  Vendor = Microsoft
  Product = Event Viewer - Application
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>1400</EventID>""", """connector failed to connect to""", """Microsoft-SharePoint Products-SharePoint Server Search""" ]
  Fields = ${DLWindowsParsersTemplates.xml-windows-events.Fields}[
    """<Message>({event_name}[^<]+)</Message>""",
    """<Data Name\\*='string0'>({additional_info}[^<]+)<""",
    """<Execution ProcessID\\*='({process_id}\d+)' ThreadID\\*='({thread_id}\d+)'\/>""",
    """<Security UserID\\*='({user_sid}[^<']+)"""
  ]

xml-windows-events = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)('|")""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
  
}
```