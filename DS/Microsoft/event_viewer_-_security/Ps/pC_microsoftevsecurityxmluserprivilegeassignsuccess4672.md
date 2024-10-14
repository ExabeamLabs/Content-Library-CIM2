#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-privilege-assign-success-4672"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
Conditions = [ """<EventID>4672</EventID>""", """SubjectUserName""" ]
Fields = [
  """<EventTime>({time}[^\<]+)<""",
  """<TimeCreated SystemTime(\\\/)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """<TimeCreated SystemTime(\\\/)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{1,9}Z)""",
  """<Computer>({host}({src_host}[\w\-.]+))</Computer>""",
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """<Keywords>({result}[^<]+)</Keywords>""",
  """<Keywords><Keyword>({result}[^<]+)</Keyword></Keywords>""",
  """<EventID>({event_code}[^<]+)</EventID>""",
  """<Data Name(\\\/)?=('|")SubjectLogonId('|")>({login_id}[^<]+)""",
  """<Data Name(\\\/)?=('|")SubjectUserName('|")>(NETWORK SERVICE|(\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>""",
  """<Data Name(\\\/)?=('|")SubjectDomainName('|")>({domain}[^<]+)</Data>""",
  """<Data Name(\\\/)?=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>""",
  """({event_name}Special privileges assigned to new logon)""",
  """<Data Name(\\\/)?=('|")PrivilegeList('|")>({privileges}[^<]+)</Data>""",
  """<Data Name(\\\/)?=('|")SubjectUserSid('|")>({user_sid}[^<]+)</Data>""",
  """<Hostname>({host}[^\.\<]+)\.({domain}[^\s\<]+)<"""
  """<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```