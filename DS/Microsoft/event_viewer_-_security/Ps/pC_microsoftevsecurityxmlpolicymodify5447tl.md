#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-policy-modify-5447-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>5447<"
    ]
    Fields = [
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)<TimeCreated SystemTime(\\\\)?='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Execution ProcessID(\\\\)?='({process_id}\\d+)"
      "(?i)<Task>({task_name}[^<]+)"
      "(?i)<Data Name(\\\\)?='UserSid'>({user_sid}[^<]+)"
      "(?i)<Data Name(\\\\)?='UserName'>(((?i)NT AUTHORITY|(({domain}[^\\\\]+)))\\\\)?((?i)LOCAL SERVICE|({user}[^<]+))"
      "(?i)<Data Name(\\\\)?='ProviderName'>({provider_name}[^<]+)"
      "(?i)<Data Name(\\\\)?='ChangeType'>({event_category}[^<]+)"
      "(?i)<Data Name(\\\\)?='Action'>({action}[^<]+)"
      "(?i)<Keywords>({result}[^<]+)"
    ]
  

}
```