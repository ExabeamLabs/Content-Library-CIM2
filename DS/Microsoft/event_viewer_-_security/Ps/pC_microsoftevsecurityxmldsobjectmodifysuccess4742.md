#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-modify-success-4742"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
Conditions = [
"""<EventID>4742</EventID>"""
"""<Data Name ='TargetSid'>"""
"""<Data Name ='TargetUserName'>"""
"""<Message>A computer account was changed"""
]
Fields = [
  """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  """<Message>({event_name}A computer account was changed)"""
  """<Computer>({host}[\w\-.]+)<"""
  """<EventID>({event_code}4742)<"""
  """<Data Name ='TargetUserName'>({dest_user}[^<]+)<"""
  """<Data Name ='TargetDomainName'>({object_dn}[^<]+)<"""
  """<Data Name ='SubjectUserName'>({user}[^<]+)<"""
  """<Data Name ='SubjectDomainName'>({domain}[^<]+)<"""
  """<Data Name ='SubjectLogonId'>({login_id}[^<]+)<"""
  """<Data Name ='UserPrincipalName'>(-|({attribute}[^<]+))<"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```