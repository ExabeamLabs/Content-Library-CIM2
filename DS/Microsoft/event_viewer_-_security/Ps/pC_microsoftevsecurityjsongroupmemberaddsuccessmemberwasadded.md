#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-group-member-add-success-memberwasadded"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """"EventID":4756"""
	""""MemberName":""""
    """A member was added to a security-enabled"""
  ]
  Fields = [
      """EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
      """({event_name}A member was added to a security-enabled [\w\s]+ group)""",
	    """"hostname":"({host}[\w\-.]+)"""",
      """({event_code}4728|4732|4756)""",
      """"SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
	    """"SubjectDomainName":"({domain}[^"]+)"""",
      """A member was added to a security-enabled ({group_type}\w+) group""",
      """"SubjectUserSid":"({user_sid}[^"]+)"""",
      """"MemberName":"CN\\*=({account}[^,]+)""",
      """"Account":"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """"MemberName":"(?:-|({user_dn}CN\\*=.+?,({user_ou}OU.+?DC\\*=[\w-]+)))?"""",
      """"TargetAccount":"(({group_domain}[^\\\s"]+)\\+)?({group_name}[^\\\s"]+)""",
      """"MemberSid":"(({dest_user_sid}S-\d+-[^\s"]+)|({account_id}[^\s"]+))""",
      """"ManagementGroupName":"({group_name}[^\s"]+)""",
      """"SubjectLogonId":"({login_id}[^\s"]+)""",
      """"TargetSid":"({group_id}[^\s"]+)""",
      """"EventType":"({result}[^"]+)""""
  ]
  DupFields = [ "host->dest_host", "user->src_user", "domain->src_domain" ]
  ParserVersion = "v1.0.0"


}
```