#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-create-success-4720"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
""""EventID":4720""",
""""SourceModuleType":"""
  ]
  Fields = [
"""({event_name}A user account was created)""",
""""EventTime":\s*"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})"""",
""""Hostname":"({host}[\w\-.]*)""",
"""({event_code}4720)""",
""""SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
""""SubjectDomainName":"({domain}[^"]+)""",
""""SubjectLogonId":"({login_id}[^"]+)"""
""""TargetSid":"({account_id}[^"]+)""",
""""TargetUserName":"({account_name}[^"]+)""",
""""TargetDomainName":"({account_domain}[^"]+)"""
  ]
  DupFields = [ "account_name->dest_user", "account_domain->dest_domain" ]


}
```