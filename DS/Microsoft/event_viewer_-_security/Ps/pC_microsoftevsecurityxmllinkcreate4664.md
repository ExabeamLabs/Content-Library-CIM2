#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-link-create-4664
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4664<""", """An attempt was made to create a hard link""" ]
  Fields = [
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Message>({event_name}[^:<\.]+)""",
    """<Message>({event_name}[^<]+?)\.(\s|<)""",
    """'SubjectUserSid'>({user_sid}[^'<\s]+)<""",
    """'SubjectUserName'>({user}[\w\.\-]{1,40}\$?)<""",
    """'SubjectDomainName'>({domain}[^'<\s]+)<""",
    """'SubjectLogonId'>({login_id}[^'<\s]+)<""",
    """'FileName'>(|({file_path}({file_dir}[^"<]*?)[\\\/]*({file_name}[^\\\/"<]+?(\.({file_ext}[^\\\/\.\s"<]+))?)))<""",
# link_name is removed
    """'TransactionId'>\{?({transaction_id}[^'<\}]+)\}?<""",
    """<EventID>({event_code}\d+)""",
    """<Keyword>({result}.+?)</Keyword>""",
  ]


}
```