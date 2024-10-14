#### Parser Content
```Java
{
Name = microsoft-windows-xml-scheduled-task-modify-success-140
  Vendor = Microsoft
  Product = Event Viewer - TaskScheduler
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>140</EventID>""", """Microsoft-Windows-TaskScheduler""" ]
  Fields = [
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)('|")""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task_name}[^<]+)""",
    """<Data Name\\*=('|")TaskName('|")>({task_name}[^<]+)<""",
    """<Data Name\\*=('|")ResultCode('|")>({result_code}[^<]+)<""",
    """<Data Name =('|")UserName('|")>(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/Data>"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```