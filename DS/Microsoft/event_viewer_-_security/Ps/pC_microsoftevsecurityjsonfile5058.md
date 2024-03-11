#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-file-5058
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """EventID":5058""", """Key file operation""" ]
  Fields = [
    """"+EventTime"+:({time}\d+)""",
    """"+EventTime"+:\s*"+({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2})"+"""
    """({event_name}Key file operation)""",
    """"+Hostname"+:"+({host}[^"]+)"+""",
    """"+EventType"+:"+({result}[^"]+)"+""",
    """"+EventID"+:({event_code}\d+)""",
    """"+SourceName"+:"+({log_source}[^"]+)"+""",
    """"+ProviderGuid"+:"+\{({process_guid}[^}]+)""",
    """"+ActivityID"+:"+\{({activity_id}[^}]+)""",
    """"+ProcessID"+:({process_id}\d+)"""
    """"+Message"+:"+({additional_info}[^"]+)""",
    """"+Category"+:"+({category}[^"]+)""",
# algorithm_name is removed
    """"+KeyName"+:"+({key_name}[^"]+)"+""",
    """"+KeyFilePath"+:"+({file_path}[^"]+)"+"""
    """"SubjectLogonId"+:"+({login_id}[^"]+)"""",
    """"SubjectUserSid"+:"+({user_sid}[^"]+)"""",
    """"SubjectUserName"+:"+({user}[^"]+)"""",
    """"Operation"+:"+({operation}[^"]+)"""",
  ]
  DupFields = [ "host->dest_host" ]


}
```