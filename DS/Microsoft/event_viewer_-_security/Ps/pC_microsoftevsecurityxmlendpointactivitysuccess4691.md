#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-activity-success-4691
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>4691</EventID>""", """<Message>Indirect access to an object was requested""" ]
  Fields = ${WindowsParsersTemplates.xml-windows-events.Fields}[
    """<Data Name\\*='SubjectUserName'>({user}[\w\.\-]{1,40}\$?)<\/Data>""",
    """<Data Name\\*='SubjectDomainName'>({domain}[^<]+)<\/Data>""",
    """<Data Name\\*='ObjectType'>({object_type}[^<]+)""",
    """<Data Name\\*='ObjectName'>({object}[^<]+)""",
    """<Data Name\\*='AccessList'>({access}[^<]+?)\s*<""",
    """<Data Name\\*='SubjectLogonId'>({login_id}[^<]+)<\/Data>""",
    """<Execution ProcessID\\*='({process_id}\d+)' ThreadID\\*='({thread_id}\d+)'\/>""",
    """<Data Name\\*='SubjectUserSid'>({user_sid}[^<]+)"""
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