#### Parser Content
```Java
{
Name = "microsoft-evsystem-xml-policy-apply-1500-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - System"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>1500</eventid>"
      "the group policy settings for the computer were processed successfully"
    ]
    Fields = [
      "(?i)({event_name}The Group Policy settings for the computer were processed successfully)"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z'\\/>"
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)<Keywords>({result}[^<]+)</Keywords>"
      "(?i)<Security UserID='({user_sid}.+?)'\\/>"
      "(?i)<EventRecordID>({event_id}[^<]+)<\\/EventRecordID>"
    ]
  

}
```