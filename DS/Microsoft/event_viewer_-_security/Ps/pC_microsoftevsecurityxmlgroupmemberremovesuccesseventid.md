#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-group-member-remove-success-eventid"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [
    """Provider Name"""
    """TargetUserName"""
    """A member was removed from a security-enabled"""
    """<EventID>"""
  ]
  Fields = [
      """({event_name}A member was removed from a security-enabled [\w\s]+ group)""",
      """SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d)\d+Z""",
      """<Computer>({dest_host}({host}[\w\-.]+))""",
      """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
      """<EventID>({event_code}[^<]+)""",
      """A member was removed from a security-enabled\s*({group_type}[^\s]+)\s+group""",
      """<Data Name =('|")MemberName('|")>(-|({user_dn}[^<]+))<""",
      """<Data Name =('|")MemberSid('|")>({dest_user_sid}[^<]+)""",
      """<Data Name =('|")SubjectUserSid('|")>({user_sid}[^"\s<]+)<""",
      """<Data Name =('|")SubjectUserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<""",
      """<Data Name =('|")SubjectDomainName('|")>({domain}[^"\s<]+)<""",
      """<Data Name =('|")SubjectLogonId('|")>({login_id}[^"\s<]+)<""",
      """CN=({account_id}.*?(?=\s*,OU))""",
      """OU=({user_ou}[^,]+)""",
      """<Data Name =('|")TargetUserName('|")>({group_name}[^<]+)""",
      """<Data Name =('|")TargetDomainName('|")>({group_domain}[^<]+)""",
      """<Data Name =('|")TargetSid('|")>({group_id}[^<]+)""",
      """<Data Name ="MemberName(">|":")CN\\?=({member}[^>]+)<\/Data>""",
      """<Data Name =('|")TargetUserName('|")>(({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}\w+(\s+\w+)+))<\/Data>""",
      """<Level>({run_level}[^<]+)<"""
      ]
  DupFields = [ "user_dn->member", "user->src_user", "domain->src_domain" ]
  ParserVersion = "v1.0.0"


}
```