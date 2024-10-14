#### Parser Content
```Java
{
Name = microsoft-windows-xml-scheduled-task-finish-success-102
  Vendor = Microsoft
  Product = Event Viewer - RemoteDesktopServices
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>102</EventID>""", """<Provider Name =""","""<Channel>Microsoft-Windows-RemoteDesktopServices""" ]
  Fields = [
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)('|")""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task_name}[^<]+)""",
    """<Level>({run_level}[^<]+)<"""
  ]


}
```