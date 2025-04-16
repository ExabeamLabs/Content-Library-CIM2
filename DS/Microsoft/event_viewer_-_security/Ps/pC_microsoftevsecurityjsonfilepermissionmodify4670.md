#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-file-permission-modify-4670
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ExtractionType = json
  Conditions = ["""EventID":4670""", """Permissions on an object were changed"""]
  Fields = [
    """exa_json_path=$.times[*].EventTime,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$.Computer,exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$.Message,exa_regex=({event_name}Permissions on an object were changed)""",
    """exa_json_path=$.EventID,exa_field_name=event_code""",
    """exa_json_path=$.Hostname,exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$..SubjectUserSid,exa_field_name=user_sid""",
    """exa_json_path=$..SubjectUserName,exa_regex=^(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
    """exa_json_path=$..SubjectDomainName,exa_field_name=domain""",
    """exa_json_path=$..SubjectLogonId,exa_field_name=login_id""",
    """exa_json_path=$..ProcessId,exa_field_name=process_id""",
    """exa_json_path=$..ProcessName,exa_regex=^({auth_process}(({process_dir}[^"]+?)\\+)?({process_name}[^"\\]+))$""",
    """exa_json_path=$..HandleId,exa_field_name=object_id""",
    """exa_json_path=$..ObjectType,exa_field_name=object_type""",
    """exa_json_path=$..ObjectName,exa_field_name=object_name,exa_match_expr=!InList($..ObjectName,"-")""",
    """exa_json_path=$..NewSd,exa_field_name=attribute""",
    """exa_json_path=$.Opcode,exa_field_name=severity"""
]
DupFields = ["user->src_user", "domain->src_domain"]  


}
```