#### Parser Content
```Java
{
Name = "microsoft-evsystem-xml-service-start-6005-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - System"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      ">6005<"
      "the event log service was started"
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
    DupFields = [
      "host->src_host"
    ]
  

}
```