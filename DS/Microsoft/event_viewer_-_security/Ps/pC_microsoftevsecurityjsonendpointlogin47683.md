#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-4768-3
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = ["""A Kerberos authentication ticket (TGT) was requested""", """Account Name""", """computer_name""", """event_id\":4768"""]
  Fields = ${DLWindowsParsersTemplates.json-windows-events-2.Fields}[
    """"(?:winlog\.)?computer_name"+:"+({src_host}[^"]+)""",
    """"TargetUserName"+:"+({dest_user}[^"]+)""",
    """"user"+:"+(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"+SubjectDomainName"+:"+({src_domain}[^"]+)""",
    """"+SubjectUserName"+:"+(SYSTEM|({src_user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"hostname"+:"+({host}[^"]+)""",
    """({event_name}A Kerberos authentication ticket \(TGT\) was requested)""",
    """TargetUserName\\?"+:\\?"(?:-|(?i)(system|anonymous logon|LOCAL SERVICE|LOCAL SYSTEM)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"""",
    """IpAddress\\?"+:\\?"(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\?"""",
    """Status\\?"+:\\?"({failure_code}({result_code}[\w\-]+))\\?"""",
    """TargetDomainName\\?"+:\\?"(?:-|({dest_domain}({domain}[^\s\\]+?)))\\?"""",
    """TargetSid\\?"+:\\?"({dest_user_sid}({user_sid}[^\\"]+))\\?""""
    """"event_id[\\]?"+:({event_code}\d+)"""
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