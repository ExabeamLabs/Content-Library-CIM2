#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-group-member-remove-memberremoved"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = [ "epoch_sec", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Conditions = [
    """"EventID":"""
    """A member was removed from a security-enabled"""
    """"MemberSid":"""
    """"MemberName":"""
  ]
  Fields = [
    """"EventTime":({time}\d{10})""",
    """"EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)""""
    """"Hostname":"({host}[\w.-]+?)"""",
    """"EventID":"*({event_code}\d+)""",
    """({event_name}A member was removed from a security-enabled ({group_type}[\w\s]+) group)""",
    """"SubjectUserName":"({user}[\w\.\-]{1,40}\$?)""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"MemberSid":"({account_id}[^"]+)""",
    """"MemberName":"({user_dn}CN=({member}[^=]+).*,({user_ou}OU=[^"]+?DC=[\w-]+?))"""",
    """"TargetUserName":"({group_name}[^"]+)""",
    """"TargetDomainName":"({group_domain}[^"]+)""",
    """"TargetSid":"({group_id}[^"]+)"""
  ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```