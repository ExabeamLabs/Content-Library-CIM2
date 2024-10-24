#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-endpoint-notification-unabletologeventstosecuritylog
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """Unable to log events to security log:""" ]
  Fields = ${WindowsParsersTemplates.windows-events.Fields}[
    """({event_name}Unable to log events to security log)""",
    """Status code:\s*({result_code}[^\s]+)""",
# CrashOnAuditFail is removed
# number_of_failed_audits is removed
  ]

windows-events = {
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