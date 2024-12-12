#### Parser Content
```Java
{
Name = microsoft-windows-xml-endpoint-notification-success-98
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>98</EventID>""", """<Provider Name =""", """<Execution ProcessID=""", """<Channel>System</Channel>""" ]
  Fields = ${WindowsParsersTemplates.xml-windows-events.Fields}[
    """<Message>({additional_info}[^<]+)</Message>""",
    """<Execution ProcessID\\*='({process_id}\d+)' ThreadID\\*='({thread_id}\d+)'\/>""",
    """<Security UserID\\*='({user_sid}[^<']+)""",
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  ]

xml-windows-events = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)('|")""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task_name}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
  
}
```