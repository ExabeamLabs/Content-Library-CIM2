#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-endpoint-notification-success-4100
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>4100</EventID>""", """<Channel>System<""", """Microsoft-Windows-Diagnostics-Networking""" ]
  Fields = ${DLWindowsParsersTemplates.xml-windows-events-dl.Fields}[
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """\sActivityID=('|")\{?({activity_id}[^\}'"]+)""",
    """\sGuid=('|")\{?({process_guid}[^\}'"]+)""",
    """<EventRecordID>({event_id}\d+)<"""
  ]

xml-windows-events-dl = {
  Vendor = Microsoft
  Product = Event Viewer - Application
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)('|")""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task_name}[^<]+)""",
    """<Execution ProcessID\\*=('|")({process_id}\d+)('|") ThreadID\\*=('|")({thread_id}\d+)('|")\/>""",
    """<Security UserID\\*=('|")({user_sid}[^<'"]+)""",
    """<Data Name\\*=('|")TaskName('|")>({task_name}[^<]+)<"""
    """<Level>({run_level}[^<]+)<""",
    """<Channel>({channel}[^<]+)<\/Channel>"""
  
}
```