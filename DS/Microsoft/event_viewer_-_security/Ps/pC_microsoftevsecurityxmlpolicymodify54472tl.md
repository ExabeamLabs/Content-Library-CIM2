#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-policy-modify-5447-2-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>5447</eventid>"
      "<task>other policy change events"
      "a windows filtering platform filter has been changed"
    ]
    Fields = [
      "(?i)({event_name}A Windows Filtering Platform filter has been changed)"
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z'\\/>"
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)Subject:.+?Security ID:\\s*({user_sid}[^\\s]+)"
      "(?i)Subject:.+?Account Name:\\s*((NT AUTHORITY|({domain}[^\\\\\\s]+))\\\\+)?(LOCAL SERVICE|({user}[^\\\\\\s]+))"
    ]
  

}
```