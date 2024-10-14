#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-close-success-4689-2
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """Event_ID="4689"""", """Task="Process Termination"""", """A process has exited""" ]
  Fields = [
    """({event_name}A process has exited)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\+\d+:\d+)\s({host}[^\s]+)""",
    """EVENT_SID="+(N\/A|({user_sid}[^\"]+))""""
    """EVENT_USERNAME="+(({domain}[^\\]+)\\+)?({src_host}[^"]+)"""
    """Logon ID:\s*({login_id}[^\s]+)""",
    """ProcessId="({process_id}[^"]+)""",
    """ProcessName ="\s*({process_path}(?:({process_dir}.+?)[\\\/]+)?\s*({process_name}[^"\\\/]+?))"""",
    """Account Name:\s*(LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:""",
    """\sExit Status:\s*({action}[^\s"]+)"""
  ]


}
```