#### Parser Content
```Java
{
Name = "microsoft-evapp-xml-endpoint-notification-3009-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Application"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>3009</eventid>"
    ]
    Fields = [
      "(?i)<Message>({event_name}.+?)\\s*\\.(\\s|</Message>)"
      "(?i)<Message>({event_name}.+?)\\s+Subject:"
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)"
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)<EventRecordID>({event_id}[^<]+)<\\/EventRecordID>"
      "(?i)<Correlation ActivityID='\\{({activity_id}[^\\}']+)"
      "(?i)<Execution ProcessID='({process_id}[^']+)"
      "(?i)ProcessID='({process_id}\\d+)"
      "(?i)ThreadID='({thread_id}[^']+)"
      "(?i)ActivityID='\\{?({activity_id}[^\\}']+)"
      "(?i)<Keywords?>({result}[^<]+)<\\/Keywords?>"
      "(?i)<Provider>({provider_name}.+?)</Provider>"
      "(?i)<Data Name ='ErrorDescription'>({failure_reason}[^<]+?)\\s*</Data>"
      "(?i)Security ID:\\s*({user_sid}\\S+)\\s+Account Name:"
      "(?i)Account Name:\\s*(LOCAL SERVICE|({user}\\S+))\\s+Account Domain:"
      "(?i)Account Domain:\\s*(NT AUTHORITY|({domain}\\S+))\\s+Logon ID:"
      "(?i)Logon ID:\\s*({login_id}\\S+)\\s+"
      "(?i)Provider Name:\\s*({provider_name}.+?)\\s+Algorithm Name:"
      "(?i)Key Name:\\s*({key_name}.+?)\\s+Key Type:"
      "(?i)Key Type:\\s*({key_type}.+?)\\s+(Key File Operation Information|Additional Information|Cryptographic Operation)"
      "(?i)File Path:\\s*({file_path}.+?)\\s+Operation:"
      "(?i)Operation:\\s*({operation}[^:]+?)\\s+Return Code:"
      "(?i)Return Code:\\s*({return_code}.+?)<\\/Message>"
      "(?i)Group:\\s*(|-|({group_name}.+?))\\s*Security ID:\\s*(|-|({group_id}.+?))\\s*Group Name:\\s*(|-|({=group_name}.+?))\\s*Group Domain:\\s*(|-|({group_domain}.+?))\\s"
      "(?i)<Data Name ='RuleId'>\\{?({rule_id}[^}<]+)"
      "(?i)<Data Name ='RuleName'>({rule}[^<]+)"
    ]
  

}
```