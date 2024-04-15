#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-move-success-5139"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [ """<EventID>5139</EventID>""", """<Event xmlns='""" ]
Fields = [
  """<Computer>({host}.+?)</Computer>""",
  """<TimeCreated SystemTime='({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z'/>""",
  """<Data Name ='SubjectLogonId'>\s*({login_id}.+?)\s*</Data>""",
  """<Data Name ='SubjectUserName'>\s*(SYSTEM|({user}[^\s]+?))\s*</Data>""",
  """<Data Name ='SubjectDomainName'>\s*({domain}[^\s]+?)\s*</Data>""",
  """<Data Name ='SubjectUserSid'>\s*({user_sid}[^\s]+?)\s*</Data>""",
  """<Data Name ='ObjectClass'>\s*({ds_object_class}.+?)\s*</Data>""",
  """<Data Name ='NewObjectDN'>\s*({src_ds_object_dn}.+?)</Data>\s*"""
  """({event_code}5139)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```