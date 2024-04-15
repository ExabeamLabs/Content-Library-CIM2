#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-service-create-success-4622-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4622<"
      "<provider name='microsoft-windows-security-auditing'"
      "a security package has been loaded by the local security authority"
    ]
    Fields = [
      "(?i)({event_code}4622)"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Keyword>({result}[^<]+)<\\/Keyword>"
      "(?i)<EventRecordID>({event_id}[^<]+)<\\/EventRecordID>"
      "(?i)({event_name}A security package has been loaded by the Local Security Authority)"
      "(?i)Message>[^\\]\\}]*?<Task>({operation}[^<]+?)<"
      "(?i)<Provider Name ='Microsoft-Windows-Security-Auditing' Guid='\\{({process_guid}[^}]+?)\\}"
      "(?i)<Correlation ActivityID='\\{({activity_id}[^\\}']+)"
      "(?i)<Execution ProcessID='({process_id}[^']+)"
      "(?i)ThreadID='({thread_id}[^']+)"
      "(?i)<Provider>({provider_name}[^<]+?)<"
      "(?i)<Data Name ='SecurityPackageName'>({service_name}[^<]+)<"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```