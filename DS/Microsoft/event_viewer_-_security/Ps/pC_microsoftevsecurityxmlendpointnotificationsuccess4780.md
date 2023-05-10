#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-success-4780
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>4780</EventID>""", """<Message>The ACL was set on accounts which are members of administrators groups""" ]
  Fields = ${WindowsParsersTemplates.xml-windows-events.Fields}[
    """<Data Name ='SubjectUserName'>({user}[^<]+)<\/Data>""",
    """<Data Name ='SubjectDomainName'>({domain}[^<]+)<\/Data>""",
    """<Data Name ='TargetUserName'>({dest_user}[^<]+)""",
    """<Data Name ='SubjectLogonId'>({login_id}[^<]+)<\/Data>""",
    """<Execution ProcessID='({process_id}\d+)' ThreadID='({thread_id}\d+)'\/>""",
    """<Data Name ='SubjectUserSid'>({user_sid}[^<]+)"""
  ]

xml-windows-events = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)'""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task}[^<]+)"""
  
}
```