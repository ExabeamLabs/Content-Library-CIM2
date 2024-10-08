#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-key-5061-2
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""<EventID>5061<""","""SubjectLogonId""", """<Data Name""" ]
  Fields = [
    """TimeCreated SystemTime(\\)?=('|")({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """<Computer>({src_host}({host}[\w\-.]+))"""
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
    """<EventID>({event_code}\d+)""",
    """<Data Name[^<>]+?SubjectUserSid[^<>]+?>({user_sid}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectUserName[^<>]+?>({user}[\w\.\-]{1,40}\$?)</Data>""",
    """<Data Name[^<>]+?SubjectDomainName[^<>]+?>({domain}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectLogonId[^<>]+?>({login_id}[^<>]+?)</Data>""",
# algorithm_name is removed
    """<Data Name(\\)?=('|")KeyName('|")>({key_name}[^<]+)""",
    """<Data Name(\\)?=('|")KeyType('|")>({key_type}[^<]+)""",
    """<Data Name(\\)?=('|")Operation('|")>({operation}[^<]+)""",
    """<Data Name(\\)?=('|")ReturnCode('|")>({return_code}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```