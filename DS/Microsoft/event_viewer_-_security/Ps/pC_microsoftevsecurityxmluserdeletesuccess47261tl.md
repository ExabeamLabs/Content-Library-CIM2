#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-delete-success-4726-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4726</eventid>"
      "<data name='targetsid'>"
    ]
    Fields = [
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)<Data Name ='SubjectUserSid'>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"
      "(?i)<Data Name ='SubjectUserName'>({user}[^<]+)</Data>"
      "(?i)<Data Name ='SubjectDomainName'>({domain}[^<]+)</Data>"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+)</Data>"
      "(?i)<Data Name ='TargetSid'>(?:NONE_MAPPED|({dest_user_sid}[^<]+))</Data>"
      "(?i)<Data Name ='TargetUserName'>(?=\\w)({dest_user}[^<]+)</Data>"
      "(?i)<Data Name ='TargetDomainName'>(?=\\w)({dest_domain}[^<]+)</Data>"
    ]
    DupFields = [
      "host->dest_host"
      "dest_user->account_name"
    ]
    ParserVersion = "v1.0.0"
  

}
```