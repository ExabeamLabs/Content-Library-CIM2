#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-member-add-success-4756-2
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  Conditions = [ """<EventID>4756</EventID>""", """<Data Name""","""'TargetSid'>""" ]
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """SystemTime(\\)?=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<EventID>({event_code}[^<]+)</EventID>""",
    """<Computer>({host}[\w\-.]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Data Name(\\)?='MemberName'>({user_dn}(?i)(cn)=({member}.+?),({user_ou}OU.+?DC=[\w-]+))</Data>""",
    """<Data Name(\\)?='TargetUserName'>(?=\w)({group_name}[^<]+)</Data>""",
    """<Data Name(\\)?='TargetDomainName'>(?=\w)({group_domain}[^<]+)</Data>""",
    """<Data Name(\\)?='TargetSid'>({group_id}[^<]+)</Data>""",
    """<Data Name(\\)?='SubjectUserSid'>({user_sid}[^<]+)</Data>""",
    """<Data Name(\\)?='SubjectUserName'>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
    """<Data Name(\\)?='SubjectDomainName'>({domain}[^<]+)</Data>""",
    """<Data Name(\\)?='SubjectLogonId'>({login_id}[^<]+)</Data>""",
    """<Data Name(\\)?='RemoteIPAddress'>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """<Data Name(\\)?='LocalIPAddress'>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<""",
    """<Data Name(\\)?='RemotePort'>({dest_port}\d+)""",
    """<Data Name(\\)?='LocalPort'>({src_port}\d+)""",
    """<Message>({additional_info}[^<]+)""",
    """<Provider>({provider_name}[^<]+)""",
    """<System>.*?Guid(\\)?='\{({process_guid}[^}]+)""",
    """<Execution ProcessID(\\)?='({process_id}\d+)""",
    """<Security UserID(\\)?='({user_sid}[^']+)""",
    """ThreadID(\\)?='({thread_id}\d+)"""
    """<Level>({run_level}[^<]+)<"""
    """<Data Name(\\)?='RemoteMachineAccount'>({dest_host}[\w\-.]+)"""
    """<Data Name ='MemberName('>|":")CN\\?=({member}[^>]+)<\/Data>""",
    """<Data Name(\\)?='MemberSid'>(({dest_user_sid}S-\d+-[^:\s<]+)|({account_domain}[^\\\s<]+)\\+({account_name}[^\s]+)|(?:[^\s\<]+))</Data>""",
  ]
  DupFields = ["user->src_user", "domain->src_domain"]


}
```