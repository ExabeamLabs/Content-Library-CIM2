#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-member-add-success-4751
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  Conditions = [ """<EventID>4751</EventID>""", """Microsoft-Windows-Security-Auditing""", """MemberSid""" ]
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{9}Z)""",
    """<EventID>({event_code}[^<]+)</EventID>""",
    """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
    """<Data Name =('|")MemberName('|")>({user_dn}(?i)(cn)=({member}.+?),({user_ou}OU.+?DC=[\w-]+))</Data>""",
    """<Data Name =('|")TargetUserName('|")>(?=\w)({group_name}[^<]+)</Data>""",
    """<Data Name =('|")TargetDomainName('|")>(?=\w)({group_domain}[^<]+)</Data>""",
    """<Data Name =('|")TargetSid('|")>({group_id}[^<]+)</Data>""",
    """<Data Name =('|")SubjectUserSid('|")>({user_sid}[^<]+)</Data>""",
    """<Data Name =('|")SubjectUserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
    """<Data Name =('|")SubjectDomainName('|")>({domain}[^<]+)</Data>""",
    """<Data Name =('|")SubjectUserName('|")>({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
    """<Data Name =('|")SubjectDomainName('|")>({src_domain}[^<]+)</Data>""",    
    """<Data Name =('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>""",
    """<System>.*?Guid(\\)?=('|")\{({process_guid}[^}]+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}\d+)""",
    """<Data Name ="MemberSid">({account_id}(?=[^\\<]+\\)({domain}[^\\]+)\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)|(?:[^\s\<]+))</Data>""",
    """<Level>({run_level}[^<]+)<"""
      ]


}
```