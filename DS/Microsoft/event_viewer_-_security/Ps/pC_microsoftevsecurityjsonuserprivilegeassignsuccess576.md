#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-user-privilege-assign-success-576
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  Conditions = [ """"Special privileges assigned to new logon""", """"event_id":576,"""]
  Fields = [
    """exa_json_path=$.message,exa_regex=({event_name}Special privileges assigned to new logon)""",
    """exa_json_path=$.@timestamp,exa_field_name=time""",
    """exa_json_path=$.computer_name,exa_regex=^({host}[\w\-\.]+)$""",
    """exa_json_path=$.event_id,exa_field_name=event_code""",
    """exa_json_path=$.message,exa_regex=({ownership_privilege}SeTakeOwnershipPrivilege)""",
    """exa_json_path=$.message,exa_regex=({environment_privilege}SeSystemEnvironmentPrivilege)""",
    """exa_json_path=$.message,exa_regex=({debug_privilege}SeDebugPrivilege)""",
    """exa_json_path=$.message,exa_regex=({tcb_privilege}SeTcbPrivilege)""",
    """exa_json_path=$.record_number,exa_field_name=event_id""",
    """exa_json_path=$.user.identifier,exa_field_name=user_sid""",
    """exa_json_path=$.user.domain,exa_field_name=domain""",
    """exa_json_path=$.user.name,exa_regex=^({user}[\w\.\-]{1,40}\$?)$""",
    """exa_json_path=$..param4,exa_field_name=privileges""",
    """exa_json_path=$..Privileges,exa_field_name=privileges""",
    """exa_json_path=$..param3,exa_regex=\(([^,\s]+(,|\s))?(-|({login_id}.+?)\))""",
    """exa_json_path=$..LogonID,exa_regex=\(([^,\s]+(,|\s))?(-|({login_id}.+?)\))""",
    """exa_json_path=$..logon_id,exa_regex=\(([^,\s]+(,|\s))?(-|({login_id}.+?)\))"""
  ]
  DupFields = ["host->dest_host"]


}
```