#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-policy-apply-success-4954
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>4954</EventID>""", """Microsoft-Windows-Security-Auditing""", """<TimeCreated SystemTime""", """<Computer>""" ]
  Fields = ${WindowsParsersTemplates.xml-windows-events.Fields}[
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """<Execution ProcessID\\*='({process_id}\d+)' ThreadID\\*='({thread_id}\d+)'\/>"""
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