#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-endpoint-logout-success-anaccountwasloggedoff-1
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"event_id":4634""", """An account was logged off""" ]
  Fields = ${DLWindowsParsersTemplates.json-windows-events-2.Fields}[
    """"TargetUserName"+:"+({dest_user}[^"]+)""",
    """"user"+:"+(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"(?:winlog\.)?computer_name"+:"+({src_host}[^"]+)""",
    """"hostname"+:"+({host}[^"]+)""",
    """({event_name}An account was logged off)""",
    """"@timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
    """"+SubjectDomainName"+:"+({src_domain}({domain}[^"]+))""",
    """"+SubjectUserName"+:"+(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
  ]

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
# algorithm_name is removed
    """"+Operation"+:"+({operation}[^"]+)""",
    """"+KeyType"+:"+({key_type}[^"]+)""",
    """"+KeyName"+:"+({key_name}[^"]+)""",
    """"+PrivilegeList"+:"+(-|({privileges}[^"]+))""",
    """"+SidHistory"+:"+(-|({sid_history}[^"]+))"""
    """exa_json_path=$.EventData.SubjectUserSid,exa_field_name=user_sid"""
    """exa_json_path=$.EventData.SubjectLogonId,exa_field_name=login_id"""
    """exa_json_path=$.EventID,exa_field_name=event_code"""
    """exa_json_path=$.EventData.ProviderName,exa_field_name=provider_name"""
    """exa_regex=@timestamp\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """exa_json_path=$.EventData.KeyType,exa_field_name=key_type"""
  
}
```