#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-activity-success-4911
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>4911</EventID>""", """Resource attributes of the object were changed""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = ${WindowsParsersTemplates.xml-windows-events.Fields}[
    """<Data Name\\*='SubjectUserName'>({user}[^<]+)<\/Data>""",
    """<Data Name\\*='SubjectDomainName'>({domain}[^<]+)<\/Data>""",
    """<Data Name\\*='ObjectType'>({object_type}[^<]+)""",
    """<Data Name\\*='ObjectName'>({object}[^<]+)""",
    """<Data Name\\*='OldSd'>({old_attribute}[^<]+)""",
    """<Data Name\\*='NewSd'>({new_attribute}[^<]+)""",
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