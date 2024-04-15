#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-logout-4647-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>4647</eventid>"
      "<task>logoff"
      "user initiated logoff"
    ]
    Fields = [
      "(?i)({event_name}User initiated logoff)"
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z'\\/>"
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)<Keywords>({result}[^<]+)</Keywords>"
      "(?i)<Data Name ='TargetUserSid'>({user_sid}[^<]+)<\\/Data>"
      "(?i)<Data Name ='TargetDomainName'>({domain}[^<]+)<\\/Data>"
      "(?i)<Data Name ='TargetUserName'>({user}[^<]+)<\\/Data>"
      "(?i)<Data Name ='TargetLogonId'>({login_id}[^<]+)<\\/Data>"
    ]
  

}
```