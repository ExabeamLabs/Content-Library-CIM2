#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-endpoint-activity-success-microsoftwindowssecurityauditing
   Product = Event Viewer - Security
   Vendor = Microsoft
   TimeFormat = [ "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss" ]
   ParserVersion = v1.0.0
   ExtractionType = json
   Conditions = [  """Microsoft-Windows-Security-Auditing[""", """"EventID":""" ]
   Fields  = [
    """exa_json_path=$.EventID,exa_field_name=event_code""",
    """exa_json_path=$.EventTime,exa_regex=({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
    """exa_json_path=$.TimeCreated,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$.Hostname,exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$.EventType,exa_field_name=result""",
    """exa_json_path=$..SubjectUserSid,exa_field_name=user_sid""",
    """exa_json_path=$..SubjectUserName,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
    """exa_json_path=$..SubjectDomainName,exa_field_name=domain""",
    """exa_json_path=$..SubjectLogonId,exa_field_name=login_id""",
    """exa_json_path=$..ProcessId,exa_field_name=process_id""",
    """exa_json_path=$..ProcessName,exa_regex=^({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$""",
    """exa_json_path=$..param1,exa_regex=^({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$""",
    """exa_json_path=$..TransactionId,exa_field_name=transaction_id""",
    """exa_json_path=$..Category,exa_field_name=event_name""",
    """exa_json_path=$..Message,exa_regex=({event_name}[^.]+)"""
    ]
   
 

}
```