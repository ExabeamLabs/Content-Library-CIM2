#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-close-processexited
  ParserVersion = v1.0.0
  Conditions = [ """A process has exited""" ]
  Fields = ${WindowsParsersTemplates.windows-events.Fields}[
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""",
    """"Computer":"({host}[^"]+)"""",
    """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
    """\d+\s+({host}[^\s]+)\sMSWinEventLog""",
    """"forwarder":"({host}[^"]+)""",
    """({event_name}A process has exited)""",
    """"EventID":({event_code}\d{1,5})""",
    """Security ID:\s*({user_sid}[^\s]+)""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"SubjectUserName":"({user}[^"]+)"""",
    """Account Name:\s*({src_host}[^\s]+)""",
    """Account Domain:\s*({domain}[^:]+?)\s+Logon ID:""",
    """Logon ID:\s*({login_id}[^\s]+)""",
    """Process ID:\s*({process_id}[^\s]+)""",
    """"ProcessName":"({process_path}(({process_dir}[^"]+?)\\+)?({process_name}[^"\\]+))"""",
    """Account Name:\s*({user}[^\s]+)""",
    """Exit Status:\s*({result}[^\s"]+)"""
  ]

windows-events = {
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