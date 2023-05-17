#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-file-5058-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""<EventID>5058<""","""SubjectLogonId""" ]
  Fields = [
    """TimeCreated SystemTime(\\)?=('|")({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """<Computer>({dest_host}({host}[^<]+))""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}\d+)""",
    """<Data Name[^<>]+?SubjectUserSid[^<>]+?>({user_sid}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectUserName[^<>]+?>({user}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectDomainName[^<>]+?>({domain}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectLogonId[^<>]+?>({login_id}[^<>]+?)</Data>""",
# algorithm_name is removed
    """<Data Name(\\)?=('|")Operation('|")>({operation}[^<]+)""",
    """<Data Name(\\)?=('|")ReturnCode('|")>({return_code}[^<]+)""",
    """<Data Name(\\)?=('|")KeyName('|")>({key_name}[^<]+)""",
    """<Data Name(\\)?=('|")KeyType('|")>({key_type}[^<]+)"""
  ]


}
```