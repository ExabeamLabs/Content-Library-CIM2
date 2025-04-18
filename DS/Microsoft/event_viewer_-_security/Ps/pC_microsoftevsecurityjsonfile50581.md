#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-file-5058-1
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss"]
  ExtractionType = json
  Conditions = [ """"EventID":"5058"""", """Key file operation""" ]
  Fields = ${DLWindowsParsersTemplates.json-windows-events-2.Fields} [
    """"(?:winlog\.)?computer_name"+:"+({src_host}[^"]+)""",
    """"hostname"+:"+({host}[^"]+)""",
    """({event_name}Key file operation)""",
    """({event_code}5058)""",
    """"Message":"({additional_info}[^"\\]+)""",
    """"Category":"({category}[^"]+)""",
# algorithm_name is removed
    """"KeyName":"({key_name}[^"]+)"+""",
    """"KeyFilePath":"({file_path}[^"]+)"+"""
    """"TimeCreated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"Computer":"({host}[^"]+)"""",
    """"Operation":"({operation}[^"]+)"""",
    """"Keywords":"({action}[^"]+)""",
    """exa_regex=({event_name}Key file operation)""",
    """exa_regex=({event_code}5058)""",
    """exa_json_path=$.EventData.KeyName,exa_field_name=key_name"""
    """exa_json_path=$.EventData.KeyFilePath,exa_field_name=file_path"""
    """exa_json_path=$.Computer,exa_field_name=host"""
    """exa_json_path=$.EventData.Operation,exa_field_name=operation"""
    """exa_json_path=$.Keywords,exa_field_name=action"""
    """exa_regex="TimeCreated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\d\d\dZ)"""
    """exa_regex="Message":"({additional_info}[^"\\]+)""",
  ]
  DupFields = [ "src_user->user", "src_domain->domain" ]

json-windows-events-2 = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s""",
    """"created\\*":\\*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """requestClientApplication=({app}[^=]+?)\s\w+=""",
    """({event_name}An account was logged off)""",
    """"keywords"+:\["+({result}[^"]+)""",
    """"pid"+:({process_id}\d+)""",
    """thread"+:[^=]+?"+id"+:({thread_id}\d+)""",
    """"TargetUserName"+:"+({dest_user}[^"]+)""",
    """"TargetDomainName"+:"+({account_domain}[^"]+)""",
    """"TargetLogonId"+:"+({login_id}[^"]+)""",
    """"LogonType"+:"+({login_type}\d+)""",
    """"TargetUserSid"+:"+({user_sid}[^"]+)""",
    """"record_id"+:({event_id}\d+)""",
    """"task"+:"+({task_name}[^"]+)""",
    """"event_id"+:({event_code}\d+)""",
    """"action"+:"+({action}[^"]+)""",
    """"os"+:[^=]+?"name"+:"+({os}[^"]+)""",
    """"SubjectLogonId"+:"+({login_id}[^"]+)""",
    """"+activity_id"+:"+\{({activity_id}[^}]+)""",
    """"+ProviderName"+:"+({provider_name}[^"]+)""",
    """"+SubjectUserSid"+:"+({user_sid}[^"]+)""",
    """"+SubjectDomainName"+:"+({src_domain}[^"]+)""",
# algorithm_name is removed
    """"+Operation"+:"+({operation}[^"]+)""",
    """"+KeyType"+:"+({key_type}[^"]+)""",
    """"+KeyName"+:"+({key_name}[^"]+)""",
    """"user"+:"+(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"+SubjectUserName"+:"+(SYSTEM|({src_user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"+PrivilegeList"+:"+(-|({privileges}[^"]+))""",
    """"+SidHistory"+:"+(-|({sid_history}[^"]+))"""
    """exa_json_path=$.EventData.SubjectUserSid,exa_field_name=user_sid"""
    """exa_json_path=$.EventData.SubjectUserName,exa_field_name=src_user"""
    """exa_json_path=$.EventData.SubjectDomainName,exa_field_name=src_domain"""
    """exa_json_path=$.EventData.SubjectLogonId,exa_field_name=login_id"""
    """exa_json_path=$.EventID,exa_field_name=event_code"""
    """exa_json_path=$.EventData.ProviderName,exa_field_name=provider_name"""
    """exa_regex=@timestamp\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """exa_json_path=$.EventData.KeyType,exa_field_name=key_type"""
  
}
```