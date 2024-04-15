#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-unlock-success-4801-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSS"
    Conditions = [
      "the workstation was unlocked"
      "<eventid>4801</eventid>"
    ]
    Fields = [
      "(?i)({event_name}The workstation was unlocked)"
      "(?i)<TimeCreated SystemTime(\\\\)?='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d.\\d\\d\\d\\d\\d\\d\\d\\d\\d)Z'\\/>"
      "(?i)<Computer>({host}[^<]+)<"
      "(?i)<EventID>({event_code}4801)"
      "(?i)Data Name(\\\\)?='TargetUserName'>({user}[^<]+)"
      "(?i)Data Name(\\\\)?='TargetDomainName'>({domain}[^<]+)"
      "(?i)Data Name(\\\\)?='TargetLogonId'>({login_id}[^<]+)"
      "(?i)Data Name(\\\\)?='TargetUserSid'>({user_sid}[^<]+)"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```