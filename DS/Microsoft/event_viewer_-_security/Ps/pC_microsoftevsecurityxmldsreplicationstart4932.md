#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-ds-replication-start-4932
  ParserVersion = v1.0.0
  Conditions = [ """Synchronization of a replica of an Active Directory naming context has begun""", """4932""" ]
  Fields = ${DLWindowsParsersTemplates.windows-events-1.Fields}[
    """Subject:.+?Security ID:\s*(|-|({user_sid}.+?))\s*Account Name:\s*(|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:\s*(|-|({domain}.+?))\s*Logon ID:\s*(|-|({login_id}\S+))\s""",
    """<Computer>(::ffff:)?({dest_host}({host}[\w\-.]+))</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
# dest_dra is removed
    """\sSession ID:\s*({session_id}\d+)""",
    """({event_name}Synchronization of a replica of an Active Directory naming context has begun)""",
# dest_dc is removed
# src_dc is removed
    """({event_code}4932)"""
  ]

windows-events-1 = {
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