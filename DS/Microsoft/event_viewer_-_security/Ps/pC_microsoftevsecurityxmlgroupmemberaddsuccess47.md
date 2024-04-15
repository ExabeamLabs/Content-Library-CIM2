#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-group-member-add-success-47"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
    """>47"""
    """>A member was added to a security-enabled""" 
  ]
  Fields = [
      """({event_name}A member was added to a security-enabled [\w\s]+ group)""",
      """SystemTime=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """<Computer>({host}[^<]+)</Computer>""",
      """<EventID>({event_code}[^<]+)</EventID>""",
      """(Success Audit|Audit Success|Information)<\d+>({host}[^<]+)<""",
      """>({event_code}\d+)<\d+>Microsoft-Windows-Security-Auditing""",
      """A member was added to a security-enabled ({group_type}[^\s]+) group""",
      """Subject:.+?Account Name:\s*(#011)*({user}[^\s#]+)\s*(#011)*\s*Account Domain""",
      """<Data Name ='SubjectUserName'>(\#011)*({user}[^\s#]+?)\s*(\#\d+)*\s*<""",
      """Subject:.+?Account Domain:\s*(\#011)*({domain}[^\s#]+?)\s*(\#011)*\s*Logon ID""",
      """Logon ID:\s*(\#011)*({login_id}[^\s#]+?)\s*(\#011)*\s*Member:""",
      """Member:.*?Security ID:\s*({account_id}(?=[^\\:]+\\)({sid_domain}[^\\:]+)\\({user_sid}[^\s]+)|(?:[^\s]+))\s*Account Name:""",
      """Member:(.+?({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+))|(?:.+?))\s*Group:""",
      """Group:\s*Security ID:\s*({group_id}.+?)\s*(Group|Account) Name""",
      """Group:.+?(Group|Account) Name:\s*(\#011)*({group_name}.+?)\s*(\#011)*\s*(Group|Account) Domain:""",
      """Group:.+?(Group|Account) Domain:\s*(\#011)*({group_domain}[^\s#]+)\s*(\#011)*\s*(Additional Information:)?""",
      """<Data Name ='SubjectUserSid'>({user_sid}[^<]+)<"""
  ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```