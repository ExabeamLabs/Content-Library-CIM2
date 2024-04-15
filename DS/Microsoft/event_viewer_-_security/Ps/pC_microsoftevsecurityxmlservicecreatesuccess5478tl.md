#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-service-create-success-5478-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>5478<"
      "<provider name='microsoft-windows-security-auditing'"
      "the ipsec policy agent service was started"
    ]
    Fields = [
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Keyword>({result}[^<]+)<\\/Keyword>"
      "(?i)<EventRecordID>({event_id}[^<]+)<\\/EventRecordID>"
      "(?i)<Message>({event_name}[^<]+)<\\/Message>"
      "(?i)Message>.*?<Task>({operation}.*?)<\\/Task>"
      "(?i)<Provider Name ='Microsoft-Windows-Security-Auditing' Guid='\\{({process_guid}[^}]+?)\\}"
      "(?i)<Correlation ActivityID='\\{({activity_id}[^\\}']+)"
      "(?i)<Execution ProcessID='({process_id}[^']+)"
      "(?i)ThreadID='({thread_id}[^']+)"
      "(?i)<Provider>({provider_name}.+?)<\\/Provider>"
      "(?i)({service_name}IPsec Policy Agent)"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```