#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-scheduled-task-disable-4701-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  Conditions = [ """<EventID>4701<""", """<Provider Name =""", """Microsoft-Windows-Security-Auditing""" ]
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Fields = [
    """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
    """SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """({event_code}4701)""",
    """<Data Name(\\)?=('|")SubjectUserSid('|")>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"""
    """<Data Name(\\)?=('|")SubjectUserName('|")>(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>"""
    """<Data Name(\\)?=('|")SubjectDomainName('|")>(?=\w)({domain}[^<]+)</Data>"""
    """<Data Name(\\)?=('|")SubjectLogonId('|")>(?=\w)({login_id}[^<]+)</Data>"""
    """<Data Name(\\)?=('|")TaskName('|")>(?=[\\\w])({task_name}[^<]+)</Data>"""
    """<Data Name(\\)?=('|")TaskContent('|")>({additional_info}[^<]+)<"""
    """<UserId>(?=\w)(({account_domain}[^\\<]*)\\)?({account_name}[^<]+)</UserId>"""
    """<Settings>\s*({additional_info}.+?)\s*</Settings>"""
    """<Triggers>\s*({triggers}.+?)\s*</Triggers>"""
    """<RunLevel>(?=\w)({run_level}[^<]+)</RunLevel>"""
    """<LogonType>(?=\w)({login_type_text}[^<]+)</LogonType>"""
    """<RegistrationInfo>.+?<Author>(?=\w)({author}[^<]+)</Author>"""
    """<RegistrationInfo>.+?<Description>(?=\w)({description}[^<]+)</Description>"""
    """ThreadID(\\)?=('|")({thread_id}\d+)"""
    """<Level>({run_level}[^<]+)<"""
  ]
  ParserVersion = v1.0.0


}
```