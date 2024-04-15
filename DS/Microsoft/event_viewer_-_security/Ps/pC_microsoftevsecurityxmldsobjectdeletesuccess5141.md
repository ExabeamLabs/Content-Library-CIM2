#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-delete-success-5141"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """<EventID>5141</EventID>""" ]
Fields = [
  """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """({event_code}5141)""",
  """<Computer>({host}[\w\-\.]+)</Computer>""",
  """<Keywords>({result}[^<]+)</Keywords>""",
  """<Data Name ='SubjectUserSid'>(|({user_sid}[^<]+?))</Data>""",
  """<Data Name ='SubjectUserName'>(|({user}[^<]+?))</Data>""",
  """<Data Name ='SubjectDomainName'>(|({domain}[^<]+?))</Data>""",
  """<Data Name ='SubjectLogonId'>(|({login_id}[^<]+?))</Data>""",
  """<Data Name ='ObjectDN'>(|({object_dn}[^<]+?))</Data>""",
  """<Data Name ='ObjectClass'>(|({ds_object_class}[^<]+?))</Data>"""
]
ParserVersion = "v1.0.0"


}
```