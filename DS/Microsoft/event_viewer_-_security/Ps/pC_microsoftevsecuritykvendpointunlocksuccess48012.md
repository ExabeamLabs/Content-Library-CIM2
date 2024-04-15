#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-unlock-success-4801-2"
Conditions = [
"""LogType="WLS""""
"""EventID="4801""""
]
ParserVersion = "v1.0.0"

s-xml-windows-member = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """SystemTime(\\)?=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<EventID>({event_code}[^<]+)</EventID>""",
    """<Computer>({host}[^<]+)<\/Computer>""",
    """<Data Name(\\)?='MemberName'>({user_dn}(?i)(cn)=.+?,({user_ou}OU.+?DC=[\w-]+))</Data>""",
    """<Data Name(\\)?='MemberSid'>({account_id}(?=[^\\<]+\\)({sid_domain}[^\\]+)\\({user_sid}[^\s]+)|(?:[^\s\<]+))</Data>""",
    """<Data Name(\\)?='TargetUserName'>(?=\w)({group_name}[^<]+)</Data>""",
    """<Data Name(\\)?='TargetDomainName'>(?=\w)({group_domain}[^<]+)</Data>""",
    """<Data Name(\\)?='TargetSid'>({group_id}[^<]+)</Data>""",
    """<Data Name(\\)?='SubjectUserSid'>({user_sid}[^<]+)</Data>""",
    """<Data Name(\\)?='SubjectUserName'>({user}[^<]+)</Data>""",
    """<Data Name(\\)?='SubjectDomainName'>({domain}[^<]+)</Data>""",
    """<Data Name(\\)?='SubjectLogonId'>({login_id}[^<]+)</Data>""",
    """<Data Name(\\)?='RemoteIPAddress'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """<Data Name(\\)?='LocalIPAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<""",
    """<Data Name(\\)?='RemotePort'>({dest_port}\d+)""",
    """<Data Name(\\)?='LocalPort'>({src_port}\d+)""",
    """<Message>({additional_info}[^<]+)""",
    """<Provider>({provider_name}[^<]+)""",
    """<System>.*?Guid(\\)?='\{({process_guid}[^}]+)""",
    """<Execution ProcessID(\\)?='({process_id}\d+)""",
    """<Security UserID(\\)?='({user_sid}[^']+)""",
    """<Message>({event_name}[^:=<.]+)\."""
  ]
  DupFields = [ "host->dest_host" 
}
```