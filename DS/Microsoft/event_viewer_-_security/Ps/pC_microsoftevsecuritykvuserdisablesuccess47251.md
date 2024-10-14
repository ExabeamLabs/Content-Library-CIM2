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
  """Computer="+({host}[\w\-.]+)""""
  """EventID="+({event_code}[^"]+)""""
  """EventRecordID="+({event_id}[^"]+)""""
  """SubjectUserSid="+({user_sid}[^"]+)""""
  """SubjectUserName ="+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """SubjectDomainName ="+({domain}[^"]+)""""
  """SubjectLogonId="+({login_id}[^"]+)""""
  """TargetSid="+({dest_user_sid}[^"]+)"""",
  """TargetUserSid="+({dest_user_sid}[^"]+)""""
  """ProviderGuid="+({process_guid}[^"]+)""""
  """TargetDomainName ="+({dest_domain}[^"]+)""""
  """TargetUserName ="+({dest_user}[^"]+)""""
  """ProviderGuid="+({process_guid}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```