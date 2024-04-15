#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-privilege-assign-success-4673-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4673</eventid>"
      "<data name"
      "<event xmlns"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime(\\\\\\/)?='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Keyword(s)?>({result}[^<]+?)</Keyword(s)?>"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)<Data Name(\\\\\\/)?='SubjectUserSid'>\\s*(({domain}[^\\\\\\/<]+)[\\\\\\/])?({user}[^<]+)</Data>"
      "(?i)<Data Name(\\\\\\/)?='SubjectUserName'>({user}[^<]+?)</Data>"
      "(?i)<Data Name(\\\\\\/)?='SubjectDomainName'>({domain}[^<]+?)</Data>"
      "(?i)<Data Name(\\\\\\/)?='SubjectLogonId'>({login_id}[^<]+?)</Data>"
      "(?i)<Data Name(\\\\\\/)?='ObjectServer'>({object_server}[^<]+?)</Data>"
      "(?i)<Data Name(\\\\\\/)?='PrivilegeList'>({privileges}[^<]+?)</Data>"
      "(?i)<Data Name(\\\\\\/)?='ProcessName'>({process_path}({process_dir}[^<]*?)({process_name}[^\\\\\\/<]+?))</Data>"
      "(?i)<Data Name(\\\\\\/)?='SubjectLogonId'>({login_id}[^<>\\s=]+)"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```