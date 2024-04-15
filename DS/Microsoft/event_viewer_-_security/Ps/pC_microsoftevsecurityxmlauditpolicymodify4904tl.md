#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-audit-policy-modify-4904-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "an attempt was made to register a security event source"
      "<eventid>4904<"
    ]
    Fields = [
      "(?i)TimeCreated SystemTime(\\\\)?='({time}\\d+-\\d+-\\d+T\\d+:\\d+:\\d+)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)<Data Name[^<>]+?SubjectUserSid[^<>]+?>({user_sid}[^<>]+?)</Data>"
      "(?i)<Data Name[^<>]+?SubjectUserName[^<>]+?>({user}[^<>]+?)</Data>"
      "(?i)<Data Name[^<>]+?SubjectDomainName[^<>]+?>({domain}[^<>]+?)</Data>"
      "(?i)<Data Name[^<>]+?SubjectLogonId[^<>]+?>({login_id}[^<>]+?)</Data>"
      "(?i)<Data Name[^<>]+?ProcessId[^<>]+?>({process_id}[^<>]+?)</Data>"
      "(?i)<Data Name[^<>]+?ProcessName[^<>]+?>(-|({process_path}({process_dir}[^<>]*?[\\\\\\/]+)?({process_name}[^<>\\\\\\/]+)))</Data>"
      "(?i)({event_name}an attempt was made to register a security event source)"
    ]
    DupFields = [
      "host-> dest_host"
    ]
  

}
```