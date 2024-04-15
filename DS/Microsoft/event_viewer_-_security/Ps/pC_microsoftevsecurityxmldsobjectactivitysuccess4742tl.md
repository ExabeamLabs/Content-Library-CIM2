#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-activity-success-4742-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>4742<"
      "コンピューター アカウントが変更されました。"
    ]
    Fields = [
      "(?i)({event_name}コンピューター アカウントが変更されました。)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)"
      "(?i)({event_code}4742)"
      "(?i)<EventRecordID>({event_id}[^<]+)"
      "(?i)'SubjectUserSid'>({user_sid}[^\"\\s<]+)<"
      "(?i)'SubjectUserName'>({user}[^\"\\s<]+)<"
      "(?i)'SubjectDomainName'>({domain}[^\"\\s<]+)<"
      "(?i)'SubjectLogonId'>({login_id}[^\"\\s<]+)<"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```