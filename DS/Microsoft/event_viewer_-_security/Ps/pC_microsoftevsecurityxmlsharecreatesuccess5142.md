#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-share-create-success-5142
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """Microsoft Windows""", """A network share object was added""", """Provider Name""","""Microsoft-Windows-Security-Auditing""", """<EventID>5142</EventID>""" ]
  Fields = [
    """<TimeCreated\s{1,100}SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{1,100}Z)""",
    """<Computer>({dest_host}({host}[^<]+))<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Data\sName\\*=('|")SubjectDomainName('|")>({domain}[^<]+)""",
    """<Data\sName\\*=('|")SubjectUserName('|")>({user}[^<]+)\$""",
    """<Data\sName\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)""",
    """<EventID>({event_code}[^<]+)""",
    """<Data\sName\\*=('|")ShareName('|")>\\\\\*\\({share_name}[^<]+)""",
    """<Data\sName\\*=('|")ShareLocalPath('|")>({share_path}[^<]+)""",
    """<Keyword>({result}[^<]+)<\/Keyword>"""
    """({event_name}A network share object was added)"""
  ]


}
```