#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-ds-object-create-success-5137
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """CEF:""", """destinationServiceName =Azure""", """EventID":5137""", """"Activity":"5137 - A directory service object was created""" ]
  Fields = [
  """({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,3}Z)"""
  """"Computer":"({host}[\w\-.]+)"""
  """({event_code}5137)"""
  """({event_name}A directory service object was created)"""
  """"SubjectLogonId":"({login_id}[^"]+)""""
  """"ManagementGroupName":"({group_name}[^"]+)""""
  """"SourceSystem":"({app}[^"]+)""""
  """"SubjectUserName":"({user}[^"]+)""""
  """"SubjectDomainName":"({domain}[^"]+)""""
  """"SubjectUserSid":"({user_sid}[^"]+)""""
  """"TenantId":"({tenant_id}[^"]+)""""
  """<Data Name\\?=\\?"ObjectClass\\?">({object_class}[^<]+?)<\/Data>"""
  """<Data Name\\?=\\?"ObjectDN\\?">({object_dn}[^<]+?)<\/Data>"""
  ]
  ParserVersion = "v1.0.0"


}
```