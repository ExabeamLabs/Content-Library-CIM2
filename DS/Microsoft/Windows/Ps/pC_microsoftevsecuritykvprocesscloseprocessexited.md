#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-close-processexited
  ParserVersion = v1.0.0
  Conditions = [ """A process has exited""" ]
  Fields = ${WindowsParsersTemplates.windows-events.Fields}[
    """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
    """\d+\s+({host}[^\s]+)\sMSWinEventLog""",
    """"forwarder":"({host}[^"]+)""",
    """({event_name}A process has exited)""",
    """Security ID:\s*({user_sid}[^\s]+)""",
    """Account Name:\s*({src_host}[^\s]+)""",
    """Account Domain:\s*({domain}[^:]+?)\s+Logon ID:""",
    """Logon ID:\s*({login_id}[^\s]+)""",
    """Process ID:\s*({process_id}[^\s]+)""",
    """Process Name:\s*({process_path}(?:({process_dir}.+?)[\\\/]+)?({process_name}[^\s\\\/]+))\s+""",
    """Account Name:\s*({user}[^\s]+)""",
    """Exit Status:\s*({result}[^\s"]+)"""
  ]

windows-events = {
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