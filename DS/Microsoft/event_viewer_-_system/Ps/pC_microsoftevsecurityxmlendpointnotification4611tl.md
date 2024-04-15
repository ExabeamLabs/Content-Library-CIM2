#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-notification-4611-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - System"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4611<"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime(\\\\)?='({time}\\d+-\\d+-\\d+T\\d+:\\d+:\\d+)"
      "(?i)<Computer>({host}[\\w\\-.]+)"
      "(?i)({event_code}4611)"
      "(?i)<EventRecordID>({event_id}[^<]+)"
      "(?i)'LogonProcessName'>({auth_process}[^<\"]+)<"
      "(?i)'SubjectUserName'>({user}[^\"\\s<]+)<"
      "(?i)'SubjectUserSid'>({user_sid}[^\"\\s<]+)<"
      "(?i)'SubjectDomainName'>({domain}[^\"\\s<]+)<"
      "(?i)'SubjectLogonId'>({login_id}[^\"\\s<]+)<"
    ]
  

}
```