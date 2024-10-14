#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-certificate-request-success-4886
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>4886</EventID>""", """<Provider""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = ${WindowsParsersTemplates.xml-windows-events.Fields}[
    """<Execution ProcessID\\*='({process_id}\d+)' ThreadID\\*='({thread_id}\d+)'\/>""",
    """<Data Name\\*='Requester'>(({domain}[^<\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<""",
    """<Data Name\\*='Attributes'>\s*({attributes}[^<]+?)\s*<"""
  ]

xml-windows-events = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Fields = [
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)('|")""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task_name}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
  
}
```