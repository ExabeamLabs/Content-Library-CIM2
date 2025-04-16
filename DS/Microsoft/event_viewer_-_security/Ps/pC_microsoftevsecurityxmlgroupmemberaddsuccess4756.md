#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-member-add-success-4756
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  Conditions = [ """<EventID>4756</EventID>""", """<Provider Name =""", """Microsoft-Windows-Security-Auditing""" ]
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Fields = [
    """SystemTime(\\)?=\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d)""",
    """<EventID>({event_code}[^<]+)</EventID>""",
    """<Computer>({host}[\w\-.]+)</Computer>""",
    """<Data Name(\\)?="MemberName">({user_dn}(?i)(cn)=({member}.+?),({user_ou}OU.+?DC=[\w-]+))</Data>""",
    """<Data Name(\\)?="TargetUserName">(?=\w)({group_name}[^<]+)</Data>""",
    """<Data Name(\\)?="TargetDomainName">(?=\w)({group_domain}[^<]+)</Data>""",
    """<Data Name(\\)?="TargetSid">({group_id}[^<]+)</Data>""",
    """<Data Name(\\)?="SubjectUserSid">({user_sid}[^<]+)</Data>""",
    """<Data Name(\\)?="SubjectUserName">({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
    """<Data Name(\\)?="SubjectDomainName">({domain}[^<]+)</Data>""",
    """<Data Name(\\)?="SubjectLogonId">({login_id}[^<]+)</Data>""",
    """<System>.*?Guid(\\)?="\{({process_guid}[^}]+)""",
    """<Execution ProcessID(\\)?="({process_id}\d+)""",
    """<Data Name ="MemberName(">|":")CN\\?=({member}[^>]+)<\/Data>""",
    """<Data Name(\\)?="MemberSid">(({dest_user_sid}S-\d+-[^:\s<]+)|({account_domain}[^\\\s<]+)\\+({account_name}[^\s]+)|(?:[^\s\<]+))</Data>""",
    """<Level>({run_level}[^<]+)<"""
      ]
  DupFields = ["user->src_user", "domain->src_domain"]    


}
```