#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-group-member-remove-success-eventid"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [
    """Security ID:"""
    """Logon ID:"""
    """A member was removed from a security-enabled"""
    """<EventID>"""
  ]
  Fields = [
      """({event_name}A member was removed from a security-enabled [\w\s]+ group)""",
      """SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d)\d+Z'""",
      """<Computer>({host}[^<]+)""",
      """<EventID>({event_code}[^<]+)""",
      """A member was removed from a security-enabled\s*({group_type}[^\s]+)\s+group""",
      """'MemberName'>(-|({user_dn}[^<]+))<""",
      """'MemberSid'>({user_sid}[^<]+)""",
      """'SubjectUserSid'>({user_sid}[^"\s<]+)<""",
      """'SubjectUserName'>({user}[^"\s<]+)<""",
      """'SubjectDomainName'>({domain}[^"\s<]+)<""",
      """'SubjectLogonId'>({login_id}[^"\s<]+)<""",
      """CN=({account_id}.*?(?=\s*,OU))""",
      """OU=({user_ou}[^,]+)""",
      """DC=({user_dn}[^,<]+)"""
      """'TargetUserName'>({group_name}[^<]+)""",
      """'TargetDomainName'>({group_domain}[^<]+)""",
      """'TargetSid'>({group_id}[^<]+)"""
  ]
  DupFields = [
    "host->dest_host"
   ]
  ParserVersion = "v1.0.0"


}
```