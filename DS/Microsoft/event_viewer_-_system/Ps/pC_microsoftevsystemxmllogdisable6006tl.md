#### Parser Content
```Java
{
Name = "microsoft-evsystem-xml-log-disable-6006-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - System"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      ">6006<"
      "the event log service was stopped"
    ]
    Fields = [
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)<EventRecordID>({event_id}\\d+)"
      "(?i)<Message>({event_name}[^:<\\.]+)"
      "(?i)<Keywords>({result}.+?)</Keywords>"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)"
      "(?i)<EventID[^<]*?>({event_code}\\d+)"
      "(?i)ThreadID='({thread_id}[^']+)"
      "(?i)ProcessID='({process_id}\\d+)"
      "(?i)Provider Name:\\s*({provider_name}.+?)\\s+Algorithm Name:"
    ]
  

}
```