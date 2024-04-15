#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-service-state-modify-4-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Sysmon"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>4</eventid>"
      "<message>sysmon service state changed:"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z'\\/>"
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)({event_name}Sysmon service state changed)"
      "(?i)<Keywords>({result}[^<]+)</Keywords>"
      "(?i)<EventRecordID>({event_id}[^<]+)<\\/EventRecordID>"
      "(?i)<Security UserID='({user_sid}.+?)'\\/>"
      "(?i)<Data Name ='State'>({state}.+?)<\\/Data>"
      "(?i)({log_name}Microsoft-Windows-Sysmon)"
    ]
  

}
```