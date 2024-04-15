#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-privilege-assign-success-4673-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """<EventID>4673</EventID>""", """<Data Name""", """<Event xmlns""" ]
Fields = [
  """<TimeCreated SystemTime[\\\/]*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """<Keyword(s)?>({result}[^<]+?)</Keyword(s)?>""",
  """<Computer>({host}[^<]+)</Computer>""",
  """<EventID>({event_code}[^<]+)</EventID>""",
  """<Data Name[\\\/]*='SubjectUserSid'>\s*(({domain}[^\\\/<]+)[\\\/])?({user}[^<]+)</Data>""",
  """<Data Name[\\\/]*='SubjectUserName'>({user}[^<]+?)</Data>""",
  """<Data Name[\\\/]*='SubjectDomainName'>({domain}[^<]+?)</Data>""",
  """<Data Name[\\\/]*='SubjectLogonId'>({login_id}[^<]+?)</Data>""",
  """<Data Name[\\\/]*='ObjectServer'>({object_server}[^<]+?)</Data>""",
  """<Data Name[\\\/]*='PrivilegeList'>({privileges}[^<]+?)</Data>""",
  """<Data Name[\\\/]*='ProcessName'>({process_path}({process_dir}[^<]*?)({process_name}[^\\\/<]+?))</Data>""",
  """<Data Name[\\\/]*='SubjectLogonId'>({login_id}[^<>\s=]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```