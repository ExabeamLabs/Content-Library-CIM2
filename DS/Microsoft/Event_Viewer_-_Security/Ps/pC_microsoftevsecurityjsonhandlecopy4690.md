#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-handle-copy-4690
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch_sec"
  Conditions = [ """"EventID":4690""", """An attempt was made to duplicate a handle to an object""" ]
  Fields = [
    """"EventTime":({time}\d{10})""",
    """"EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"Hostname":"({host}[\w.-]+?)"""",
    """"EventID":({event_code}\d+)""",
    """({event_name}An attempt was made to duplicate a handle to an object)"""
    """"SubjectUserName":"({user}[^"]+)""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"Keywords":({result}[^,]+)"""
# src_handle_id is removed
# src_pid is removed
# target_handle_id is removed
    """"TargetProcessId":"({dest_process_id}[^"]+)""",
    """"ProcessID":({process_id}\d+)""",
    """"ThreadID":({thread_id}\d+)"""
  ]
  DupFields = [ "host->dest_host" ]


}
```