#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-activity-success-4911
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>4911</EventID>""", """<Data Name =""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = ${WindowsParsersTemplates.xml-windows-events.Fields}[
    """<Data Name\\*=('|")SubjectUserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>""",
    """<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)<\/Data>""",
    """<Data Name\\*=('|")ObjectType('|")>({object_type}File)</Data><Data Name\\*=('|")ObjectName('|")>(-|({file_path}({file_dir}[^<]*?)({file_name}[^<\\\/]+?(\.({file_ext}[^<\\\/\.]+?))?)))<""",
    """<Data Name\\*=('|")OldSd('|")>({old_attribute}[^<]+)""",
    """<Data Name\\*=('|")NewSd('|")>({new_attribute}[^<]+)""",
    """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)<\/Data>""",
    """<Execution ProcessID\\*=('|")({process_id}\d+)('|") ThreadID\\*=('|")({thread_id}\d+)('|")\/>""",
    """<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)""",
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  ]
  DupFields = ["user->src_user", "domain->src_domain"]

xml-windows-events = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)('|")""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task_name}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
  
}
```