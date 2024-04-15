#### Parser Content
```Java
{
Name = "windows-evsystem-xml-endpoint-notification-12-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - System"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>12<"
      "<provider>microsoft-windows-wininit"
      "was started as a protected process with level:"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)"
      "(?i)<Computer>({host}[\\w\\-.]+)"
      "(?i)<EventID>({event_code}12)<"
      "(?i)<Message>({event_name}[^<]+)<"
      "(?i)<EventRecordID>({event_id}\\d+)<"
      "(?i)<Execution ProcessID='({process_id}\\d+)'"
      "(?i)ThreadID='({thread_id}\\d+)'"
      "(?i)<Security UserID='({user_sid}[^']+)'"
      "(?i)<Provider>({provider_name}[^<]+)<"
      "(?i)<Message>({process_name}\\S+)\\swas started as a protected process with level"
    ]
    DupFields = [
      "host->dest_host"
    ]
  

}
```