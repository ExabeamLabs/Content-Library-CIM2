#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-success-4692
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>4692<""", """<Task>""","""Microsoft-Windows-Security-Auditing""" ]
  Fields = ${WindowsParsersTemplates.xml-windows-events.Fields}[
    """<Data Name\\*='SubjectUserSid'>({user_sid}[^<]+)<\/Data>""",
    """<Data Name\\*='SubjectDomainName'>({domain}[^<]+)<\/Data>""",
    """<Data Name\\*='SubjectUserName'>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>"""
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