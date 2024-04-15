#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-group-member-list-4799-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4799<"
    ]
    Fields = [
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)({event_name}A security-enabled local group membership was enumerated)"
      "(?i)<TimeCreated SystemTime(\\\\)?='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Data Name(\\\\)?='SubjectUserSid'>({user_sid}[^<]+)"
      "(?i)<Data Name(\\\\)?='SubjectUserName'>({user}[^<]+)"
      "(?i)<Data Name(\\\\)?='SubjectDomainName'>({domain}[^<]+)"
      "(?i)<Data Name(\\\\)?='SubjectLogonId'>({login_id}[^<]+)"
      "(?i)<Data Name(\\\\)?='TargetSid'>({group_id}[^<]+)"
      "(?i)<Data Name(\\\\)?='TargetUserName'>({group_name}[^<]+)"
      "(?i)<Data Name(\\\\)?='TargetDomainName'>({group_domain}[^<]+)"
      "(?i)<Data Name(\\\\)?='CallerProcessId'>({process_id}[^<]+)"
      "(?i)<Data Name(\\\\)?='CallerProcessName'>({process_path}({process_dir}[^<]*?[\\\\\\/]+)?({process_name}[^<\\\\\\/]+))<\\/Data>"
    ]
  

}
```