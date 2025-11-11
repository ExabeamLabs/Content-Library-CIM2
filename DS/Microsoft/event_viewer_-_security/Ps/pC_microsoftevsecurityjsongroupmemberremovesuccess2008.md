#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-group-member-remove-success-2008
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = v1.0.0
  Conditions = [ """"computer_name":""", """"provider_name":"Microsoft-Windows-Security-Auditing""", """A member was removed from a security-enabled""", """ cs6=""", """"event_id":4729""" ]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s""",
    """"+created"+:"+({time}[^"]+)""",
    """requestClientApplication=({app}[^=]+?)\s\w+=""",
    """"keywords"+:\["+({result}[^"]+)""",
    """"pid"+:({process_id}\d+)""",
    """thread"+:[^@]+?"+id"+:({thread_id}\d+)""",
    """"TargetUserName"+:"+(None|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}[^"]+))"""",
    """"TargetDomainName"+:"+({dest_domain}[^"]+)""",
    """"TargetLogonId"+:"+({dest_login_id}[^"]+)""",
    """"LogonType"+:"+({login_type}\d+)""",
    """"TargetUserSid"+:"+({dest_user_sid}[^"<,]+)""",
    """"record_id"+:({event_id}\d+)""",
    """"task"+:"+({task_name}[^"]+)""",
    """"event_id"+:({event_code}\d+)""",
    """"(?:winlog\.)?computer_name"+:"+({src_host}[^"]+)""",
    """"hostname"+:"+({host}[^"]+)""",
    """"action"+:"+({action}[^"]+)""",
    """"os":[^@]+?"name":"({os}[^"]+)""",
    """"SubjectLogonId"+:"+({login_id}[^"]+)""",
    """"+activity_id"+:"+\{({activity_id}[^}]+)""",
    """"+ProviderName"+:"+({provider_name}[^"]+)""",
    """"+SubjectUserSid"+:"+({user_sid}[^"<,]+)""",
    """"+SubjectDomainName"+:"+({src_domain}({domain}[^"]+))""",
    """"user"+:"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """"+SubjectUserName"+:"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """"+PrivilegeList"+:"+(-|({privileges}[^"]+))""",
    """"+SidHistory"+:"+(-|({sid_history}[^"]+))""",
	  """({event_name}A member was removed from a security-enabled)""",
    """"event_id":({event_code}\d+)""",
    """"+group"+:.+?name"+:"+({group_name}[^"]+)""",
    """"+group"+:.+?domain"+:"+({group_domain}[^"]+)""",
    """"+MemberSid"+:"+(({dest_user_sid}S-\d+-[^"]+)|({account_id}[^"]+))""",
    """"+MemberName"+:"+CN\\*=({account_id}[^,"]+)""",
    """"+MemberName"+:"+CN\\*=({user_dn}[^,"]+)""",
  ]


}
```