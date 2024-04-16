#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-delete-success-5141"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """<EventID>5141</EventID>""" ]
Fields = [
  """({event_name}A directory service object was deleted)""",
  """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """({event_code}5141)""",
  """<Computer>({host}[\w\-\.]+)</Computer>""",
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """<Keywords>({result}[^<]+)</Keywords>""",
  """<Data Name\\*='SubjectUserSid'>(|({user_sid}[^<]+?))</Data>""",
  """<Data Name\\*='SubjectUserName'>(|({user}[\w\.\-]{1,40}\$?))</Data>""",
  """<Data Name\\*='SubjectDomainName'>(|({domain}[^<]+?))</Data>""",
  """<Data Name\\*='SubjectLogonId'>(|({login_id}[^<]+?))</Data>""",
  """<Data Name\\*='ObjectDN'>(|({ds_object_dn}[^<]+?))</Data>""",
  """<Data Name\\*='ObjectClass'>(|({ds_object_class}[^<]+?))</Data>"""
  """<Data Name\\*='DSName'>(|({ds_name}[^<]+?))</Data>"""
  """<Data Name\\*='DSType'>(|({ds_type}[^<]+?))</Data>"""
  """<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```