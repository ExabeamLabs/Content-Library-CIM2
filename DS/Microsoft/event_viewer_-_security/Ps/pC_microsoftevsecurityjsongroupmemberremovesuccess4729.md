#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-group-member-remove-success-4729"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"SourceName":"Microsoft-Windows-Security-Auditing"""", """"EventID":4729""", """"Category":"Security Group Management"""" ]
  Fields = [
    """"EventTime":\s*"({time}\d{1,4}-\d{1,2}-\d{1,2} \d{1,2}:\d{1,2}:\d{1,2})"""",
    """"Hostname":"({dest_host}({host}[\w\-.]*))"""",
    """"EventID":({event_code}[^,]+)""",
    """"RecordNumber":({event_id}[^,]+)""",
    """"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"SubjectDomainName":"({src_domain}({domain}[^"]+))""",
    """"SubjectLogonId":"({login_id}[^"]+)""",
    """"TargetUserName":"({group_name}[^"]+)""",
    """"TargetDomainName":"({group_domain}[^"]+)""",
    """"TargetSid":\s*"({group_id}[^"]+)"""",
    """"MemberSid":"(({dest_user_sid}S-\d+-[^\s"]+)|({account_id}[^\s"]+))""",
    """"MemberName":"({user_dn}[^"]+)""",
    """"MemberName":"CN\\?=({member}[^,]+),({user_ou}OU\\?=.+?DC\\?=.+?[^"]+)"""
    """"Channel":"({channel}[^"]+)""""
    """"ProcessID":({process_id}\d+)""",
  ]
  ParserVersion = "v1.0.0"


}
```