#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-process-close-5-1-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Sysmon"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>5</eventid>"
      "<message>process terminated:"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z'\\/>"
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)({event_name}Process terminated)"
      "(?i)<Keywords>({result}[^<]+)</Keywords>"
      "(?i)<EventRecordID>({event_id}[^<]+)<\\/EventRecordID>"
      "(?i)<Security UserID='({user_sid}.+?)'\\/>"
      "(?i)<Data Name ='ProcessGuid'>\\{({process_guid}[^\\}]+)"
      "(?i)<Data Name ='ProcessId'>({process_id}.+?)<\\/Data>"
      "(?i)<Data Name ='Image'>({process_path}({process_dir}(?:[^<]+)?[\\\\\\/])?({process_name}[^\\\\\\/<]+?))<\\/Data>"
      "(?i)({log_name}Microsoft-Windows-Sysmon)"
    ]
    DupFields = [
      "host->dest_host"
      "process_guid->process_id"
    ]
  

}
```