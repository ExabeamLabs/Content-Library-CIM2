#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-group-modify-success-4735-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - System"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4735<"
      "a security-enabled local group was changed"
    ]
    Fields = [
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)({event_name}A security-enabled local group was changed.)"
      "(?i)<TimeCreated SystemTime(\\\\)?='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Execution ProcessID(\\\\)?='({process_id}\\d+)' ThreadID(\\\\)?='({thread_id}\\d+)'"
      "(?i)<EventRecordID>({event_id}\\d+)"
      "(?i)<Data Name(\\\\)?='TargetSid'>({group_id}[^<]+)"
      "(?i)<Data Name(\\\\)?='TargetUserName'>({group_name}[^<]+)"
      "(?i)<Data Name(\\\\)?='TargetDomainName'>({group_domain}[^<]+)"
      "(?i)<Data Name(\\\\)?='SubjectUserSid'>({user_sid}[^<]+)"
      "(?i)<Data Name(\\\\)?='SubjectUserName'>({user}[^<]+)"
      "(?i)<Data Name(\\\\)?='SubjectDomainName'>({domain}[^<]+)"
      "(?i)<Data Name(\\\\)?='SubjectLogonId'>({login_id}[^<]+)"
    ]
  

}
```