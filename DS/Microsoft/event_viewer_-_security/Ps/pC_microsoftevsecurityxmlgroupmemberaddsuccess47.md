#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-group-member-add-success-47"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
    """>47"""
    """Microsoft-Windows-Security-Auditing"""
    """<Task>Security Group Management<"""
    """>A member was added to a security-enabled"""
  ]
  Fields = [
      """({event_name}A member was added to a security-enabled [\w\s]+ group)""",
      """SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
      """<EventID>({event_code}[^<]+)</EventID>""",
      """(Success Audit|Audit Success|Information)<\d+>({dest_host}({host}[\w\-.]+))<""",
       """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
      """>({event_code}\d+)<\d+>Microsoft-Windows-Security-Auditing""",
      """A member was added to a security-enabled ({group_type}[^\s]+) group""",
      """Subject:.+?Account Name:\s*(#011)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(#011)*\s*Account Domain""",
      """<Data Name\\*=('|")SubjectUserName('|")>(\#011)*({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\#\d+)*\s*<""",
      """Subject:.+?Account Domain:\s*(\#011)*({domain}[^\s#]+?)\s*(\#011)*\s*Logon ID""",
      """Logon ID:\s*(\#011)*({login_id}[^\s#]+?)\s*(\#011)*\s*Member:""",
      """Member:.*?Security ID:\s*(({dest_user_sid}S-\d+-[^\s]+)|({account_domain}[^\\:]+)\\+({account_name}[^\s]+)|(?:[^\s]+))\s*Account Name:""",
      """Member:(.+?({member}({user_dn}CN\\*=.+?,({user_ou}OU.+?DC\\*=[\w-]+)))|(?:.+?))\s*Group:""",
      """Group:\s*Security ID:\s*({group_id}.+?)\s*(Group|Account) Name""",
      """Group:.+?(Group|Account) Name:\s*(\#011)*({group_name}.+?)\s*(\#011)*\s*(Group|Account) Domain:""",
      """Group:.+?(Group|Account) Domain:\s*(\#011)*({group_domain}[^\s#]+)\s*(\#011)*\s*(Additional Information:)?""",
      """<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)<""",
      """<Data Name\\*=('|")TargetUserName('|")>({dest_user}[^<]+)<\/Data>""",
      """hostname\\*=({src_host}[^\\=]+?),.*?\\="""
      """<Level>({run_level}[^<]+)<"""
  ]
  ParserVersion = "v1.0.0"


}
```