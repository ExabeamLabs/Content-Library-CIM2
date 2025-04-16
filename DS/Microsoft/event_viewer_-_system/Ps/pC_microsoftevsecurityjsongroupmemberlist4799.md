#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-group-member-list-4799
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""A security-enabled local group membership was enumerated""", """"EventID":4799"""]
  Fields = [
    """({event_name}A security-enabled local group membership was enumerated)""",
    """({event_code}4799)""",
    """"EventTime":({time}\d+)""",
    """"EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"Hostname":"({host}[^"]+)"""",
    """"SeverityValue":({severity}\d+)""",
    """"SeverityValue":"({severity}[^"]+)"""",
    """"SubjectUserSid":"({user_sid}[^"]+)"""",
    """"SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"LogonID":"({login_id}[^"]+)"""",
    """"TargetUserName":"({group_name}[^"]+)"""",
    """"TargetS(?i)ID":"({group_id}[^"]+)"""",
    """"TargetDomainName":"({group_domain}[^"]+)"""",
    """"CallerProcessId":"({process_id}[^"]+)"""",
    """"CallerProcessName":"({process_path}({process_dir}[^,"]+?[\\\/]+)?({process_name}[^\\\/\s"]+?))""""
  ]
  DupFields = ["user->src_user", "domain->src_domain"]


}
```