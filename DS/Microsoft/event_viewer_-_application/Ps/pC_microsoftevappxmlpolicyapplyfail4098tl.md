#### Parser Content
```Java
{
Name = "microsoft-evapp-xml-policy-apply-fail-4098-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Application"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "4098</eventid>"
      "group policy object did not apply"
    ]
    Fields = [
      "(?i)({event_name}Group Policy Object did not apply)"
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z'\\/>"
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)({event_code}4098)"
      "(?i)<Keywords>({result}[^<]+)</Keywords>"
      "(?i)<Security UserID='({user_sid}.+?)'\\/>"
      "(?i)<EventRecordID>({event_id}[^<]+)<\\/EventRecordID>"
      "(?i)error code '({error_code}[^\\s]+)\\s"
    ]
  

}
```