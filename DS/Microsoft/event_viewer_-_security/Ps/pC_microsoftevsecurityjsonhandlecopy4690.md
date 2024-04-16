#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-handle-copy-4690
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ExtractionType = json
  Conditions = [ """"EventID":4690""", """An attempt was made to duplicate a handle to an object""" ]
  Fields = [
    """"EventTime":({time}\d{10})""",
    """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",    
    """"Hostname":"({host}[\w.-]+?)"""",
    """"EventID":({event_code}\d+)""",
    """({event_name}An attempt was made to duplicate a handle to an object)"""
    """"SubjectUserName":"({user}[\w\.\-]{1,40}\$?)""",
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
    """exa_json_path=$.Hostname,exa_field_name=host"""
    """exa_json_path=$.EventID,exa_field_name=event_code"""
    """exa_json_path=$.Message,exa_field_name=event_name"""
    """exa_json_path=$.Properties.SubjectUserName,exa_field_name=user"""
    """exa_json_path=$.Properties.SubjectDomainName,exa_field_name=domain"""
    """exa_json_path=$.Properties.SubjectLogonId,exa_field_name=login_id"""
    """exa_json_path=$.Properties.SubjectUserSid,exa_field_name=user_sid"""
    """exa_json_path=$.Keywords,exa_field_name=result"""
    """exa_json_path=$.Properties.TargetProcessId,exa_field_name=dest_process_id"""
    """exa_json_path=$.ProcessId,exa_field_name=process_id"""
    """exa_json_path=$.ThreadId,exa_field_name=thread_id"""
    """exa_regex="EventTime":({time}\d{10})""",
    """exa_regex="EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  ]
  DupFields = [ "host->dest_host" ]


}
```