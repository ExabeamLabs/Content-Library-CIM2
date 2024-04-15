#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-alert-trigger-success-4649-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>4649</eventid>"
      "a replay attack was detected"
    ]
    Fields = [
      "(?i)<EventRecordID>({event_id}[^<]+)<\\/EventRecordID>"
      "(?i)ThreadID='({thread_id}[^']+)"
      "(?i)Account Domain:\\s*(NT AUTHORITY|({domain}\\S+))\\s+Logon ID:"
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)<Execution ProcessID='({process_id}[^']+)"
      "(?i)ProcessID='({process_id}\\d+)"
      "(?i)Name ='LogonProcessName'>({auth_process}[^<]+)"
      "(?i)<Message>({event_name}.+?)\\s*\\.(\\s|</Message>)"
      "(?i)<Message>({event_name}.+?)\\s+Subject:"
      "(?i)<Keywords?>({result}[^<]+)<\\/Keywords?>"
      "(?i)<Provider>({provider_name}.+?)</Provider>"
      "(?i)<Correlation ActivityID='\\{({activity_id}[^\\}']+)"
      "(?i)ActivityID='\\{?({activity_id}[^\\}']+)"
      "(?i)Security ID:\\s*({user_sid}\\S+)\\s+Account Name:"
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)"
      "(?i)Logon ID:\\s*({login_id}\\S+)\\s+"
      "(?i)Account Name:\\s*(LOCAL SERVICE|({user}\\S+))\\s+Account Domain:"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)({additional_info}Credentials Which Were Replayed:.+)This event indicates that a Kerberos replay attack was detected"
    ]
    DupFields = [
      "event_name->alert_name"
      "auth_process->alert_type"
    ]
    ParserVersion = "v1.0.0"
  

}
```