#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-group-member-add-success-sourcemoduletype"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
      """"Message":"A member was added to a security-enabled """
      """"SourceModuleType":"""
   ]
  Fields = [
    """({event_name}A member was added to a security-enabled [\w\s]+ group)""",
    """"EventTime":\s+"({time}\d{1,4}-\d{1,2}-\d{1,2} \d{1,2}:\d{1,2}:\d{1,2})"""",
    """"Hostname":"({host}[^."]*)""",
    """"EventID":({event_code}[^,]+)""",
    """"RecordNumber":({event_id}[^,]+)""",
    """"Message":"A member was added to a security-enabled ({group_type}[^\s]+) group.""",
    """"SubjectUserName":"({user}[^"]+)""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"SubjectDomainName":"({domain}[^"]+)""",
    """"SubjectLogonId":"({login_id}[^"]+)""",
    """"TargetUserName":"({group_name}[^"]+)""",
    """"TargetDomainName":"({group_domain}[^"]+)""",
    """"MemberSid":"({account_id}[^"]+)""",
    """"MemberName":"({user_dn}[^"]+)""",
    """"MemberName":"CN=.*,({user_ou}OU=.+?DC=.+?[^"]+)""",
  ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```