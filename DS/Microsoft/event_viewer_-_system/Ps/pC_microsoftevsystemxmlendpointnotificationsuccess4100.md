#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-endpoint-notification-success-4100
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>4100</EventID>""", """<Channel>System<""", """Microsoft-Windows-Diagnostics-Networking""" ]
  Fields = ${DLWindowsParsersTemplates.xml-windows-events.Fields}[
    """\sActivityID=('|")\{?({activity_id}[^\}'"]+)""",
    """\sGuid=('|")\{?({process_guid}[^\}'"]+)""",
    """<EventRecordID>({event_id}\d+)<"""
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