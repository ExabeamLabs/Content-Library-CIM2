#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-lock-success-4740-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4740</eventid>"
      "<data name='targetsid'>"
    ]
    Fields = [
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)<Data Name ='SubjectUserName'>({src_user}[^<]+)</Data>"
      "(?i)<Data Name ='SubjectDomainName'>({domain}[^<]+)</Data>"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+)</Data>"
      "(?i)<Data Name ='TargetSid'>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"
      "(?i)<Data Name ='TargetUserName'>(?=\\w)({user}[^<]+)</Data>"
      "(?i)<Data Name ='SubjectDomainName'>(?=\\w)({domain}[^<]+)</Data>"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```