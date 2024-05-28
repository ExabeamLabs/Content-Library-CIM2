#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-logout-4634-2
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ExtractionType = json
  Conditions = [ """"EventID":"4634"""", """An account was logged off""" ]
  Fields = [
    """({event_name}An account was logged off)""",
    """({event_code}4634)""",
    """"systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """"TimeCreated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"Computer":"({src_host}({host}[\w\-.]+))"""",
    """"Keywords":"({result}[^"]+)""",
    """"TargetUserName":"({user}[\w\.\-]{1,40}\$?)"""",
    """"TargetLogonId":"({login_id}[^"]+)"""",
    """"TargetDomainName":"({domain}[^"]+)"""",
    """"TargetUserSid":"({user_sid}[^"]+)"""",
    """"eventRecordID":"({event_id}\d+)""",
    """"severityValue":"({action}[^"]+?)\s*"""",
    """"logonType":"({login_type}\d+)\s*""""
    """exa_regex=({event_name}An account was logged off)""",
    """exa_regex=({event_code}4634)""",
    """exa_json_path=$..systemTime,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$..TimeCreated,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$..Computer,exa_regex=^({src_host}({host}[\w\-.]+))$""",
    """exa_json_path=$..Keywords,exa_field_name=result""",
    """exa_json_path=$..TargetUserName,exa_regex=^({user}[\w\.\-]{1,40}\$?)$""",
    """exa_json_path=$..TargetLogonId,exa_field_name=login_id""",
    """exa_json_path=$..TargetDomainName,exa_field_name=domain""",
    """exa_json_path=$..TargetUserSid,exa_field_name=user_sid""",
    """exa_json_path=$..EventRecordID,exa_field_name=event_id""",
    """exa_json_path=$..severityValue,exa_field_name=action""",
    """exa_json_path=$..LogonType,exa_field_name=login_type"""
  ]


}
```