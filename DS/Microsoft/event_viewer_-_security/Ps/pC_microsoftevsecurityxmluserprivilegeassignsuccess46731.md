#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-privilege-assign-success-4673-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
Conditions = [ """<EventID>4673</EventID>""", """<Data Name""" ]
Fields = [
  """<TimeCreated SystemTime[\\\/]*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """<TimeCreated SystemTime[\\\/]*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{1,9}Z)""",
  """<Keyword(s)?>({result}[^<]+?)</Keyword(s)?>""",
  """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """<EventID>({event_code}[^<]+)</EventID>""",
  """<Data Name[\\\/]*=('|")SubjectUserSid('|")>\s*(({domain}[^\\\/<]+)[\\\/])?({user}[\w\.\-]{1,40}\$?)</Data>""",
  """<Data Name[\\\/]*=('|")SubjectUserName('|")>({user}[\w\.\-]{1,40}\$?)</Data>""",
  """<Data Name[\\\/]*=('|")SubjectDomainName('|")>({domain}[^<]+?)</Data>""",
  """<Data Name[\\\/]*=('|")SubjectLogonId('|")>({login_id}[^<]+?)</Data>""",
  """<Data Name[\\\/]*=('|")ObjectServer('|")>({object_server}[^<]+?)</Data>""",
  """<Data Name[\\\/]*=('|")PrivilegeList('|")>({privileges}[^<]+?)</Data>""",
  """<Data Name[\\\/]*=('|")ProcessName('|")>({process_path}({process_dir}(?:[^"<]*?)?[\\\/])?)({process_name}[^\\\/"<]+?)</Data>""",
  """<Data Name[\\\/]*=('|")SubjectLogonId('|")>({login_id}[^<>\s=]+)"""
  """({event_name}A privileged service was called)"""
  """<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```