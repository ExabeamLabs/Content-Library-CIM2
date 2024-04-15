#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-privilege-assign-success-4672-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4672</eventid>"
      "'subjectusername'>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime(\\\\\\/)?='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}({dest_host}[\\w\\-]+)[^<]*)</Computer>"
      "(?i)<Keywords>({result}[^<]+)</Keywords>"
      "(?i)<Keywords><Keyword>({result}[^<]+)</Keyword></Keywords>"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)<Data Name(\\\\\\/)?='SubjectLogonId'>({login_id}[^<]+)"
      "(?i)<Data Name(\\\\\\/)?='SubjectUserName'>(SYSTEM|NETWORK SERVICE|({user}[^<]+))</Data>"
      "(?i)<Data Name(\\\\\\/)?='SubjectDomainName'>(?:NT AUTHORITY|({domain}[^<]+))</Data>"
      "(?i)<Data Name(\\\\\\/)?='SubjectLogonId'>({login_id}[^<]+)</Data>"
      "(?i)({event_name}Special privileges assigned to new logon)"
      "(?i)<Data Name(\\\\\\/)?='PrivilegeList'>({privileges}[^<]+)</Data>"
      "(?i)<Data Name(\\\\\\/)?='SubjectUserSid'>({user_sid}[^<]+)</Data>"
    ]
    ParserVersion = "v1.0.0"
  

}
```