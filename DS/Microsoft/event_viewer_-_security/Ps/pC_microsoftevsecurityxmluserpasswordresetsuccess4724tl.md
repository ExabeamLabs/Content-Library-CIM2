#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-password-reset-success-4724-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4724</eventid>"
      "<data name='targetsid'>"
    ]
    Fields = [
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}({dest_host}[\\w-]+)[^<]*)</Computer>"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)<Data Name ='TargetSid'>(?:NONE_MAPPED|({dest_user_sid}[^<]+))</Data>"
      "(?i)<Data Name ='TargetUserName'>(?=\\w)({dest_user}[^<]+)</Data>"
      "(?i)<Data Name ='TargetDomainName'>(?=\\w)({dest_domain}[^<]+)</Data>"
      "(?i)<Data Name ='SubjectUserSid'>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"
      "(?i)<Data Name ='SubjectUserName'>(?=\\w)({user}[^<]+)</Data>"
      "(?i)<Data Name ='SubjectDomainName'>(?=\\w)({domain}[^<]+)</Data>"
      "(?i)<Data Name ='SubjectLogonId'>(?=\\w)({login_id}[^<]+)</Data>"
      "(?i)<Keyword>({result}[^<]+?)<\\/Keyword>"
      "(?i)({event_name}An attempt was made to reset an account's password)"
    ]
    ParserVersion = "v1.0.0"
  

}
```