#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-close-success-4689-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """EVENT_ID="4689"""", """EVENT_TASK="Process Termination"""", """A process has exited""" ]
  Fields = [
    """({event_name}A process has exited)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\+\d+:\d+)\s({host}[^\s]+)""",
    """EVENT_SID="+(N\/A|({user_sid}[^\"]+))""""
    """EVENT_USERNAME="+(({domain}[^\\]+)\\+)?({src_host}[^"]+)"""
    """Logon ID:\s*({login_id}[^\s]+)""",
    """Process ID:\s*({process_id}[^\s]+)""",
    """Process Name:\s*({process_path}(?:({process_dir}.+?)[\\\/]+)?\s*({process_name}[^\s\\\/]+))\s+""",
    """Account Name:\s*(LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:""",
    """\sExit Status:\s*({action}[^\s"]+)"""
  ]


}
```