#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-group-member-add-success-eventid47"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [
    """<EventID>47"""
    """>A member was added to a security-enabled"""
    """<Provider Name ="""
  ]
  Fields = [
    """({event_name}A member was added to a security-enabled [\w\s]+ group)""",
    """<TimeCreated SystemTime='({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)""",
    """<Computer>({host}[^<]+)</Computer>""",
    """<EventID>({event_code}[^<]+)</EventID>""",
    """A member was added to a security-enabled ({group_type}[^\s]+) group""",
    """<Data Name ='SubjectUserSid'>({user_sid}[^<]+)<"""
    """<Data Name ='SubjectUserName'>({user}[\w\.\-]{1,40}\$?)""",
    """<Data Name ='SubjectDomainName'>({domain}[^<]+)<""",
    """<Data Name ='SubjectLogonId'>({login_id}[^<]+)<""",
    """<Data Name ='MemberSid'>({account_id}[^<]+)<""",
    """<Data Name =('|")TargetDomainName('|")>({group_domain}[^<]+)<""",
    """<Data Name =('|")TargetSid('|")>({group_id}[^<]+)<"""
    """<Data Name =('|")TargetUserName('|")>({group_name}[^<]+)<""",
    """<Data Name(\\)?=('|")MemberName('|")>({user_dn}(?i)(cn)=({member}.+?),({user_ou}OU.+?DC=[\w-]+))<\/Data>"""
    """Member:(.+?({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+))|(?:.+?))\s*Group:"""
  ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```