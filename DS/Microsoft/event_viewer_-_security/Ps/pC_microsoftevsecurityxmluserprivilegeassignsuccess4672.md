#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-privilege-assign-success-4672"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """<EventID>4672</EventID>""", """'SubjectUserName'>""" ]
Fields = [
  """<TimeCreated SystemTime(\\\/)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """<Computer>({host}({dest_host}[\w\-]+)[^<]*)</Computer>""",
  """<Keywords>({result}[^<]+)</Keywords>""",
  """<Keywords><Keyword>({result}[^<]+)</Keyword></Keywords>""",
  """<EventID>({event_code}[^<]+)</EventID>""",
  """<Data Name(\\\/)?='SubjectLogonId'>({login_id}[^<]+)""",
  """<Data Name(\\\/)?='SubjectUserName'>(SYSTEM|NETWORK SERVICE|({user}[^<]+))</Data>""",
  """<Data Name(\\\/)?='SubjectDomainName'>(?:NT AUTHORITY|({domain}[^<]+))</Data>""",
  """<Data Name(\\\/)?='SubjectLogonId'>({login_id}[^<]+)</Data>""",
  """({event_name}Special privileges assigned to new logon)""",
  """<Data Name(\\\/)?='PrivilegeList'>({privileges}[^<]+)</Data>""",
  """<Data Name(\\\/)?='SubjectUserSid'>({user_sid}[^<]+)</Data>"""
]
ParserVersion = "v1.0.0"


}
```