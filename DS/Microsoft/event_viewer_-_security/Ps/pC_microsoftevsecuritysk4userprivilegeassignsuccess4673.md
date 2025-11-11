#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-user-privilege-assign-success-4673
  ParserVersion = v1.0.0
  Conditions = [ """"event_id":4673""", """A privileged service was called""" ]
  Fields = ${WindowsParsersTemplates.json-windows-events-1.Fields}[
    """"(?:winlog\.)?computer_name"+:"+({src_host}[\w\-.]+)""",
    """"hostname"+:"+({host}[\w\-.]+)""",
    """"TargetUserName"+:"+(None|({dest_user}[^"]+))""",
    """"user"+:"+(SYSTEM|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"+SubjectUserName"+:"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """"TargetDomainName"+:"+({dest_domain}[^"]+)""",
    """"+SubjectDomainName"+:"+({src_domain}({domain}[^"]+))""",
    """exa_json_path=$.winlog.event_data.TargetDomainName,exa_field_name=dest_domain""",
    """exa_json_path=$.winlog.event_data.SubjectDomainName,exa_field_name=domain""",
    """exa_json_path=$.winlog.event_data.SubjectDomainName,exa_field_name=src_domain""",
    """exa_json_path=$.winlog.event_data.TargetUserName,exa_field_name=dest_user""",
    """exa_json_path=$.winlog.event_data.SubjectUserName,exa_field_name=user""",
    """exa_json_path=$.winlog.event_data.SubjectUserName,exa_field_name=src_user""",
    """exa_json_path=$.winlog.computer_name,exa_field_name=src_host""",
    """exa_json_path=$.host.hostname,exa_field_name=host""",
    """({event_name}A privileged service was called)""",
    """"PrivilegeList"+:"+({privileges}[^"]+)""",
    """"ObjectServer"+:"+({object_server}[^"]+)""",
    """"ProcessName"+:"+({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?))"""",
    """"ProcessId"+:"+({process_id}[^"]+)""",
    """"hostname"+:"+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({dest_host}[\w\-.]+))""",
    """"SubjectUserName":"({dest_user}[^"]+)""""
  ]

json-windows-events-1 = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s""",
    """"+created"+:"+({time}[^"]+)""",
    """requestClientApplication=({app}[^=]+?)\s\w+=""",
    """({event_name}An account was logged off)""",
    """"keywords"+:\["+({result}[^"]+)""",
    """"pid"+:({process_id}\d+)""",
    """thread"+:[^@]+?"+id"+:({thread_id}\d+)""",
    """"TargetLogonId"+:"+({dest_login_id}[^"]+)""",
    """"LogonType"+:"+({login_type}\d+)""",
    """"TargetUserSid"+:"+({dest_user_sid}[^"<,]+)""",
    """"record_id"+:({event_id}\d+)""",
    """"task"+:"+({task_name}[^"]+)""",
    """"event_id"+:({event_code}\d+)""",
    """"action"+:"+({action}[^"]+)""",
    """"os":[^@]+?"name":"({os}[^"]+)""",
    """"SubjectLogonId"+:"+({login_id}[^"]+)""",
    """"+activity_id"+:"+\{({activity_id}[^}]+)""",
    """"+ProviderName"+:"+({provider_name}[^"]+)""",
    """"+SubjectUserSid"+:"+({user_sid}[^"<,]+)""",
    """"+PrivilegeList"+:"+(-|({privileges}[^"]+))""",
    """"+SidHistory"+:"+(-|({sid_history}[^"]+))""",
    """"Keywords":"({result}[^"]+)"""

      """exa_regex=\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s"""
      """exa_json_path=$.event.created,exa_field_name=time"""
      """exa_regex=({event_name}An account was logged off)"""
      """exa_json_path=$.winlog.keywords,exa_field_name=result"""
      """exa_json_path=$.winlog.process.pid,exa_field_name=process_id"""
      """exa_json_path=$.winlog.process.thread.id,exa_field_name=thread_id"""
      """exa_json_path=$.winlog.event_data.TargetLogonId,exa_field_name=dest_login_id"""
      #"""exa_json_path=$.LogonType,exa_field_name=login_type"""
      """exa_json_path=$.winlog.event_data.TargetUserSid,exa_field_name=dest_user_sid"""
      """exa_json_path=$.winlog.record_id,exa_field_name=event_id"""
      """exa_json_path=$.winlog.task,exa_field_name=task_name"""
      """exa_json_path=$.winlog.event_id,exa_field_name=event_code"""
      """exa_json_path=$.event.action,exa_field_name=action"""
      """exa_json_path=$.host.os.name,exa_field_name=os"""
      """exa_json_path=$.winlog.event_data.SubjectLogonId,exa_field_name=login_id"""
      #"""exa_json_path=$.activity_id,exa_field_name=activity_id"""
      #"""exa_json_path=$.ProviderName,exa_field_name=provider_name"""
      """exa_json_path=$.winlog.provider_name,exa_field_name=provider_name"""
      """exa_json_path=$.winlog.event_data.SubjectUserSid,exa_field_name=user_sid"""
      #"""exa_json_path=$.user,exa_field_name=user"""
      #"""exa_json_path=$.PrivilegeList,exa_field_name=privileges"""
      #"""exa_json_path=$.SidHistory,exa_field_name=sid_history"""
      #"""exa_json_path=$.Keywords,exa_field_name=result"""
  
}
```