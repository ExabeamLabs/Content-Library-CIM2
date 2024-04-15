#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-lock-success-4800-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>4800"
      "the workstation was locked"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime(\\\\)?='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d.\\d\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)({event_name}The workstation was locked)"
      "(?i)({event_code}4800)"
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