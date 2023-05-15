#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-modify-success-4735-3
 Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """<EventID>4735</EventID>""", """<Computer>""", """<Data Name""","""'SubjectUserName'>""","""'TargetUserName'>""" ]
  Fields = ${WindowsParsersTemplates.xml-windows-events.Fields}[
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)'""",
    """<Data Name\\*='SubjectUserName'>({user}[^<]+)<\/Data>""",
    """<Data Name\\*='SubjectDomainName'>({domain}[^<]+)<\/Data>""",
    """<Data Name\\*='SubjectLogonId'>({login_id}[^<]+)<\/Data>""",
    """<Data Name\\*='SubjectUserSid'>({user_sid}[^<]+)"""
    """<Data Name\\*='TargetUserName'>({group_name}[^<]+)""",
    """<Data Name\\*='TargetSid'>({group_id}[^<]+)""",
    """<Data Name\\*='TargetUserName'>({group_name}[^<]+)""",
    """<Execution ProcessID\\*='({process_id}\d+)' ThreadID\\*='({thread_id}\d+)'\/>""",
  ]

xml-windows-events = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)'""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task}[^<]+)"""
  
}
```