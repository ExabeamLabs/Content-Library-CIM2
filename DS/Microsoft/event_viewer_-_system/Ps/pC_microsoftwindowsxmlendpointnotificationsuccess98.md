#### Parser Content
```Java
{
Name = microsoft-windows-xml-endpoint-notification-success-98
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>98</EventID>""", """<Message>Volume Windows""", """is healthy.  No action is needed""" ]
  Fields = ${WindowsParsersTemplates.xml-windows-events.Fields}[
    """<Message>({additional_info}[^<]+)</Message>""",
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
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)'""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task}[^<]+)"""
  
}
```