#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-password-modify-4723-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4723</eventid>"
      "<data name='privilegelist'>"
    ]
    Fields = [
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)<Keywords>({result}[^<]+)</Keywords>"
      "(?i)<Keyword>({result}Audit\\s[^<]+)</Keyword>"
      "(?i)<Data Name ='SubjectUserSid'>({user_sid}[^<]+)</Data>"
      "(?i)<Data Name ='SubjectUserName'>({user}[^<]+)</Data>"
      "(?i)<Data Name ='SubjectDomainName'>({domain}[^<]+)</Data>"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+)</Data>"
      "(?i)<Data Name ='TargetSid'>({dest_user_sid}[^<]+)</Data>"
      "(?i)<Data Name ='TargetUserName'>({dest_user}[^<]+)</Data>"
      "(?i)<Data Name ='TargetDomainName'>({dest_domain}[^<]+)</Data>"
      "(?i)({event_name}an attempt was made to change an account's password)"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```