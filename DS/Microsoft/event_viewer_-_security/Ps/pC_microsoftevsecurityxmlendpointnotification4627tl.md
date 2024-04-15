#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-notification-4627-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>4627</eventid>"
      "<task>group membership"
      "group membership information"
    ]
    Fields = [
      "(?i)({event_name}Group membership information)"
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)"
      "(?i)<Computer>({host}[^<>]+?)<"
      "(?i)<EventID>({event_code}[^<]+?)<"
      "(?i)<Data Name ='SubjectUserSid'>({user_sid}[^<]+)<"
      "(?i)<Data Name ='SubjectUserName'>(-|({account_name}[^<]+))<"
      "(?i)<Data Name ='SubjectDomainName'>(-|({account_domain}[^<]+))<"
      "(?i)<Data Name ='SubjectLogonId'>(-|({login_id}[^<]+))<"
      "(?i)<Data Name ='TargetUserSid'>({user_sid}[^<]+)<"
      "(?i)<Data Name ='TargetUserName'>({user}[^<]+)<"
      "(?i)<Data Name ='TargetDomainName'>({domain}[^<]+)<"
      "(?i)<Data Name ='TargetLogonId'>({login_id}[^<]+)<"
      "(?i)<Data Name ='LogonType'>({login_type}\\d+)<"
    ]
  

}
```