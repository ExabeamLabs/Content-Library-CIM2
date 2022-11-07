#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-disable-success-4725-1
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """LogType="WLS""""
  """EventID="4725""""
]
Fields = [
  """Computer="+({dest_host}[^"]+)""""
  """EventID="+({event_code}[^"]+)""""
  """EventRecordID="+({event_id}[^"]+)""""
  """SubjectUserSid="+({user_sid}[^"]+)""""
  """SubjectUserName ="+({user}[^"]+)""""
  """SubjectDomainName ="+({domain}[^"]+)""""
  """SubjectLogonId="+({login_id}[^"]+)""""
  """TargetSid="+({user_sid}[^"]+)""""
  """TargetDomainName ="+({dest_domain}[^"]+)""""
  """TargetUserName ="+({dest_user}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```