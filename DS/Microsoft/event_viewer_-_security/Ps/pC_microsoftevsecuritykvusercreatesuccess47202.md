#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-create-success-4720-2
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss"]
Conditions = [
  """LogType="WLS""""
  """EventID="4720""""
]
Fields = [
  """Computer="+({host}[^"]+)""""
  """({time}\w+\s+\d+ \d+:\d+:\d+)"""
  """"({time}\d\d\d\d\-\d+\-\d+T\d\d:\d\d:\d\d)"""
  """EventID="+({event_code}[^"]+)""""
  """EventRecordID="+({event_id}[^"]+)""""
  """SubjectUserName ="+({user}[\w\.\-]{1,40}\$?)""""
  """SubjectUserSid="+({user_sid}[^"]+)""""
  """SubjectDomainName ="+({domain}[^"]+)""""
  """SubjectLogonId="+({login_id}[^"]+)""""
  """TargetUserName ="+({account_name}[^"]+)""""
  """TargetDomainName ="+({account_domain}[^"]+)""""
  """TargetSid="+({account_id}[^"]+)""""
  """Enabled.*?'({user_type}[^']+)"""
  """ProviderGuid="+({process_guid}[^"]+)""""
]
DupFields = [
  "account_name->dest_user"
  "account_domain->dest_domain"
  "dest_user->account_name"
]
ParserVersion = "v1.0.0"


}
```