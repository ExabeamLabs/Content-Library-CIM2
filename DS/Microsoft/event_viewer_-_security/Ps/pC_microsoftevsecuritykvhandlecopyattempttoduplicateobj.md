#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-handle-copy-attempttoduplicateobj
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = [ """An attempt was made to duplicate a handle to an object""" ]
  Fields = ${WindowsParsersTemplates.windows-events.Fields}[
# src_handle_id is removed
    """Source Process ID:\s*({src_process_id}[^\s]+)\s+New Handle Information:""",
# target_handle_id is removed
    """Target Process ID:\s*({dest_process_id}[^\s<]+)""",
    """({event_name}An attempt was made to duplicate a handle to an object)""",
    """Logon ID:\s*({login_id}[^\s]+)""",
    """Account Domain:\s*({domain}[^\s]+)""",
    """Account Name:\s*({src_host}[^\s]+)""",
    """Security ID:\s*({user_sid}[^\s]+)"""
  ]

windows-events = {
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