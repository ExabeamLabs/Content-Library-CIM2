#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-ds-object-create-success-5137
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [  """EventID":5137""", """"Activity":"5137 - A directory service object was created""" ]
  Fields = [
  """({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,3}Z)"""
  """"Computer":"({host}[\w\-.]+)"""
  """({event_code}5137)"""
  """({event_name}A directory service object was created)"""
  """"SubjectLogonId":"({login_id}[^"]+)""""
  """"ManagementGroupName":"({group_name}[^"]+)""""
  """"SourceSystem":"({app}[^"]+)""""
  """"SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """"SubjectDomainName":"({domain}[^"]+)""""
  """"SubjectUserSid":"({user_sid}[^"]+)""""
  """"TenantId":"({tenant_id}[^"]+)""""
  """<Data Name\\?=\\?"ObjectClass\\?">({object_type}[^<]+?)<\/Data>"""
  """<Data Name\\?=\\?"ObjectDN\\?">({ds_object_dn}[^<]+?)<\/Data>"""
  ]
  DupFields = ["user->src_user", "domain->src_domain"]
  ParserVersion = "v1.0.0"


}
```