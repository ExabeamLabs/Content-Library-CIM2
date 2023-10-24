#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-move-success-5139"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [ """<EventID>5139</EventID>""", """<Event xmlns=""" ]
Fields = [
  """<Computer>({host}[\w\-.]+?)</Computer>""",
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
  """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z('|")/>""",
  """<Data Name\\*=('|")SubjectLogonId('|")>\s*({login_id}.+?)\s*</Data>""",
  """<Data Name\\*=('|")SubjectUserName('|")>\s*(SYSTEM|({user}[\w\.\-]{1,40}\$?))\s*</Data>""",
  """<Data Name\\*=('|")SubjectDomainName('|")>\s*({domain}[^\s]+?)\s*</Data>""",
  """<Data Name\\*=('|")SubjectUserSid('|")>\s*({user_sid}[^\s]+?)\s*</Data>""",
  """<Data Name\\*=('|")ObjectClass('|")>\s*({ds_object_class}.+?)\s*</Data>""",
  """<Data Name\\*=('|")NewObjectDN('|")>\s*({src_ds_object_dn}.+?)</Data>\s*"""
  """<Data Name\\*=('|")DSType('|")>\s*({ds_type}.+?)</Data>\s*"""
  """<Data Name\\*=('|")DSName('|")>\s*({ds_name}.+?)</Data>\s*"""
  """({event_code}5139)"""
  """<Data Name\\*=('|")ObjectGUID('|")>\{({guid}[^<\}]+)\}<"""
]
DupFields = [ "src_ds_object_dn->ds_object_dn" ]
ParserVersion = "v1.0.0"


}
```