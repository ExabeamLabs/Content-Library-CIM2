#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-success-2581
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>2581</EventID>""", """appears to be malfunctioning and will be reinitialized""", """Microsoft-SharePoint Products-SharePoint Server Search""" ]
  Fields = ${WindowsParsersTemplates.xml-windows-events.Fields}[
    """<Data Name ='string0'>({additional_info}[^<]+)<""",
    """<Execution ProcessID='({process_id}\d+)' ThreadID='({thread_id}\d+)'\/>""",
    """<Security UserID='({user_sid}[^<']+)"""
  ]

xml-windows-events = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)'""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task}[^<]+)"""
  
}
```