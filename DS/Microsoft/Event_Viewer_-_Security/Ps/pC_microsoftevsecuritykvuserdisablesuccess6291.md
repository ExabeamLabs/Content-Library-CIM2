#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-disable-success-629-1
Conditions = [
  """LogType="WLS""""
  """EventID="629""""
]
ParserVersion = "v1.0.0"

s-xml-windows-member = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """SystemTime(\\)?=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<EventID>({event_code}[^<]+)</EventID>""",
    """<Computer>({host}[^<]+)</Computer>""",
    """<Data Name(\\)?='MemberName'>({user_dn}(?i)(cn)=.+?,({user_ou}OU.+?DC=[\w-]+))</Data>""",
    """<Data Name(\\)?='MemberSid'>({account_id}(?=[^\\<]+\\)({sid_domain}[^\\]+)\\({user_sid}[^\s]+)|(?:[^\s\<]+))</Data>""",
    """<Data Name(\\)?='TargetUserName'>(?=\w)({group_name}[^<]+)</Data>""",
    """<Data Name(\\)?='TargetDomainName'>(?=\w)({group_domain}[^<]+)</Data>""",
    """<Data Name(\\)?='TargetSid'>({group_id}[^<]+)</Data>""",
    """<Data Name(\\)?='SubjectUserSid'>({user_sid}[^<]+)</Data>""",
    """<Data Name(\\)?='SubjectUserName'>({user}[^<]+)</Data>""",
    """<Data Name(\\)?='SubjectDomainName'>({domain}[^<]+)</Data>""",
    """<Data Name(\\)?='SubjectLogonId'>({login_id}[^<]+)</Data>""",
    """<Data Name(\\)?='RemoteIPAddress'>({dest_ip}[^<]+)""",
    """<Data Name(\\)?='LocalIPAddress'>({src_ip}[a-fA-F:\d.]+)<""",
    """<Data Name(\\)?='RemotePort'>({dest_port}\d+)""",
    """<Data Name(\\)?='LocalPort'>({src_port}\d+)""",
    """<Message>({additional_info}[^<]+)""",
    """<Provider>({provider_name}[^<]+)""",
    """<System>.*?Guid(\\)?='\{({process_guid}[^}]+)""",
    """<Execution ProcessID(\\)?='({process_id}\d+)""",
    """<Security UserID(\\)?='({user_sid}[^']+)""",
  ]
  DupFields = [ "host->dest_host" 
}
```