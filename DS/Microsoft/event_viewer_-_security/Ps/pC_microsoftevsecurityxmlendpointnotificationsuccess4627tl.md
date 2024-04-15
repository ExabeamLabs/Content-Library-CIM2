#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-notification-success-4627-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>4627</eventid>"
      "name='groupmembership'"
      "targetusername"
    ]
    Fields = [
      "(?i)({event_name}GroupMembership)"
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z'\\/>"
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)<Data Name ='SubjectUserSid'>({user_sid}[^<]+)<"
      "(?i)<Data Name ='TargetUserSid'>({user_sid}[^<]+)<"
      "(?i)<Data Name ='TargetLogonId'>({login_id}[^<]+)<"
      "(?i)<Data Name ='TargetUserName'>({user}[^<]+)<"
      "(?i)<Data Name ='LogonType'>({login_type}\\d+)<"
      "(?i)ProcessID='({process_id}\\d+)'"
      "(?i)ThreadID='({thread_id}\\d+)'"
      "(?i)<Keywords>({action}[^<]+)<"
      "(?i)<EventRecordID>({event_id}\\d+)"
      "(?i)<Data Name ='TargetDomainName'>({domain}[^<]+)<"
    ]
  

}
```