#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-unlock-success-4767-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>4767</eventid>"
      "<event xmlns='"
    ]
    Fields = [
      "(?i)<Computer>({host}.+?)</Computer>"
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z'/>"
      "(?i)<Data Name ='SubjectLogonId'>\\s*({login_id}.+?)\\s*</Data>"
      "(?i)<Data Name ='SubjectUserName'>\\s*(SYSTEM|({user}[^\\s]+?))\\s*</Data>"
      "(?i)<Data Name ='SubjectDomainName'>\\s*({domain}[^\\s]+?)\\s*</Data>"
      "(?i)<Data Name ='SubjectUserSid'>\\s*({user_sid}[^\\s]+?)\\s*</Data>"
      "(?i)<Data Name ='TargetDomainName'>\\s*({dest_domain}[^\\s]+?)\\s*</Data>"
      "(?i)<Data Name ='TargetUserName'>\\s*({dest_user}[^\\s]+?)\\s*</Data>"
      "(?i)<Data Name ='TargetSid'>\\s*({dest_user_sid}.+?)</Data>\\s*"
      "(?i)({event_code}4767)"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```