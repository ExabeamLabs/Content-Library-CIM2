#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-member-add-success-4756-tl
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  Conditions = [ """<eventid>4756</eventid>""", """<data name='targetsid'>""" ]
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """(?i)SystemTime(\\)?=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """(?i)<EventID>({event_code}[^<]+)</EventID>""",
    """(?i)<Computer>({host}[^<]+)</Computer>""",
    """(?i)<Data Name(\\)?='MemberName'>({user_dn}(?i)(cn)=.+?,({user_ou}OU.+?DC=[\w-]+))</Data>""",
    """(?i)<Data Name(\\)?='MemberSid'>({account_id}(?=[^\\<]+\\)({sid_domain}[^\\]+)\\({user_sid}[^\s]+)|(?:[^\s\<]+))</Data>""",
    """(?i)<Data Name(\\)?='TargetUserName'>(?=\w)({group_name}[^<]+)</Data>""",
    """(?i)<Data Name(\\)?='TargetDomainName'>(?=\w)({group_domain}[^<]+)</Data>""",
    """(?i)<Data Name(\\)?='TargetSid'>({group_id}[^<]+)</Data>""",
    """(?i)<Data Name(\\)?='SubjectUserSid'>({user_sid}[^<]+)</Data>""",
    """(?i)<Data Name(\\)?='SubjectUserName'>({user}[^<]+)</Data>""",
    """(?i)<Data Name(\\)?='SubjectDomainName'>({domain}[^<]+)</Data>""",
    """(?i)<Data Name(\\)?='SubjectLogonId'>({login_id}[^<]+)</Data>""",
    """(?i)<Data Name(\\)?='RemoteIPAddress'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?""",
    """(?i)<Data Name(\\)?='LocalIPAddress'>({src_ip}[a-fA-F:\d.]+)<""",
    """(?i)<Data Name(\\)?='RemotePort'>({dest_port}\d+)""",
    """(?i)<Data Name(\\)?='LocalPort'>({src_port}\d+)""",
    """(?i)<Message>({additional_info}[^<]+)""",
    """(?i)<Provider>({provider_name}[^<]+)""",
    """(?i)<System>.*?Guid(\\)?='\{({process_guid}[^}]+)""",
    """(?i)<Execution ProcessID(\\)?='({process_id}\d+)""",
    """(?i)<Security UserID(\\)?='({user_sid}[^']+)""",
    """(?i)<Data Name(\\)?='RemoteMachineAccount'>({dest_host}[^<]+)"""
      ]
  DupFields = [ "host->dest_host" ]


}
```