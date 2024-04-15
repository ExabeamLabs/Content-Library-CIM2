#### Parser Content
```Java
{
Name = "microsoft-evsecurity-str-group-member-remove-success-memberwasremoved"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch_sec"
  Conditions = [
    """A member was removed from a security-enabled"""
    """EventID="""
  ]
  Fields = [
      """({event_name}A member was removed from a security-enabled ({group_type}[\w\s]+) group)""",
      """EventID="*({event_code}\d+)""",
      """({host}[^\s]+)\sMicrosoft-Windows-Security-Auditing""",
      """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d[+-]\d\d:\d\d)\s+({host}[\w.-]+)\s""",
      """TimeGenerated=({time}\d{10})""",
      """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
      """Computer=({host}[^\s]+)""",
      """"SubjectDomainName":"({domain}[^"]+)"""",
      """"SubjectUserName":"({user}[^"]+)"""",
      """"SubjectLogonId":"({login_id}[^"]+)"""",
      """"SubjectUserSid":"({user_sid}[^"]+)"""",
      """"TargetDomainName":"({group_domain}[^"]+)"""",
      """"TargetUserName":"({group_name}[^"]+)"""",
      """"TargetSid":"({group_id}[^"]+)"""",
      """"MemberSid":"({user_sid}[^"]+)"""",
      """"MemberName":"(-|({user_dn}({account_id}[^"]+)))"""",
      """A member was removed from a security-enabled ({group_type}[^\s]+) group.+?Account Name:\s+({user}[^\s]+).+?Account Domain:\s+({domain}[^\s]+).+?Logon ID:\s+({login_id}[^\s]+)\s+""",
      """Member:\s+Security ID:\s+({account_id}(?=[^\\]+\\)({sid_domain}[^\\]+)\\({user_sid}[^:]+?)|(?:[^:]+?))\s+Account Name:\s+({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+))?[\w-]*\s+Group:\s+Security ID:\s+({group_id}[^\s]+).+?\s+(Group|Account) Name:\s+({group_name}[^\s]+)?.+?\s+(Group|Account) Domain:\s+({group_domain}[^\s]+)""",
  ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```