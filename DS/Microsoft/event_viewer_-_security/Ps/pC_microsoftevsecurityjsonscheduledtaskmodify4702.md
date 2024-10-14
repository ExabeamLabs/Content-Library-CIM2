#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-scheduled-task-modify-4702
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"EventID":4702""", """A scheduled task was updated""",""""TaskName":"""" ]
  Fields = [
    """"EventTime":({time}\d{10})""",
    """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"Hostname":"({host}[\w.-]+?)"""",
    """"EventID":({event_code}\d+)""",
    """({event_name}A scheduled task was updated)""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"TaskName":"({task_name}[^"]+)"""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"Keywords":"({result}[^,"]+)""",
    """<RunLevel>({run_level}[^<]+)<\/RunLevel>""",
    """<Command>({process_path}({process_dir}[^<]+)\\\\({process_name}[^<]+))<""",
    """<RegistrationInfo>[^=]+?<Description>(?=\w)({additional_info}[^=]+?)</Description>""",
    """exa_regex="EventTime":({time}\d{10})""",
    """exa_regex="EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """exa_regex=({event_code}4702)"""
    """exa_json_path=$.Hostname,exa_field_name=host"""
    """exa_json_path=$.EventID,exa_field_name=event_code"""
    """exa_regex=({event_name}A scheduled task was updated)""",
    """exa_json_path=$..SubjectUserSid,exa_field_name=user_sid"""
    """exa_json_path=$..SubjectUserName,exa_field_name=user"""
    """exa_json_path=$..SubjectDomainName,exa_field_name=domain"""
    """exa_json_path=$..TaskName,exa_field_name=task_name"""
    """exa_json_path=$..SubjectLogonId,exa_field_name=login_id"""
    """exa_json_path=$.Keywords,exa_field_name=result"""
    """exa_json_path=$.LevelDisplayName,exa_field_name=run_level"""
    """exa_regex=<Command>({process_path}({process_dir}[^<]+)\\\\({process_name}[^<]+))<""",
    """exa_regex=<RegistrationInfo>[^=]+?<Description>(?=\w)({additional_info}[^=]+?)</Description>""",
  ]
  DupFields = [ "host->dest_host" ]


}
```