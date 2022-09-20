#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-app-notification-431
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  Conditions = [ """>431</EventID>""", """<TimeCreated SystemTime=""" ]

s-xml-events = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Fields = [
    """<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({host}[^<>]+)<""",
    """<Message>({event_name}[^:<\.]+)""",
    """<Message>({event_name}[^<]+?)\.(\s|<)""",
    """<Message>({additional_info}[^<]+?)\s*<""",
    """<Message>Process '?({process_name}[^\s']+)""",
    """<Security UserID(\\)?='({user_sid}[^']+)""",
# update_path is removed
    """<Execution ProcessID(\\)?='({process_id}[^']+)""",
    """<EventID[^<]*?>({event_code}\d+)""",
    """<Keyword>({result}[^<]+)<""",
    """<Data Name(\\)?='ProcessName'>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+))</Data>""",
    """<Data Name ='TargetProcessName'>({dest_process_path}({dest_process_dir}[^<>]*?[\\\/]+)?({dest_process_name}[^<>\\\/]+))</Data>""",
    """<Data Name(\\)?='ProcessId'>({process_id}[^<]+?)\s*<""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Account Name:\s*(LOCAL SERVICE|-|({user}\S+))\s+Account Domain:""",
    """Account Domain:\s*(NT AUTHORITY|-|({domain}\S+))\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+""",
    """Task Name:\s*(|-|({task_name}[^:]+?))\s*Task Content:""",
    """Client IP: ({src_ip}[a-fA-F:\.\d]+)""",
    """ThreadID(\\)?='({thread_id}\d+)"""
  
}
```