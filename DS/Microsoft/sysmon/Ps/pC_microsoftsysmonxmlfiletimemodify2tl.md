#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-file-time-modify-2-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Sysmon"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>2</eventid>"
      "<message>file creation time changed:"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z'\\/>"
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)({event_name}File creation time changed)"
      "(?i)<Keywords>({result}[^<]+)</Keywords>"
      "(?i)<EventRecordID>({event_id}[^<]+)<\\/EventRecordID>"
      "(?i)<Security UserID='({user_sid}[^>]+?)'\\/>"
      "(?i)<Data Name ='ProcessGuid'>\\{({process_guid}[^\\}]+)"
      "(?i)<Data Name ='ProcessId'>({process_id}[^<]+?)<\\/Data>"
      "(?i)<Data Name ='Image'>({process_path}({process_dir}(?:[^<]+)?[\\\\\\/])?({process_name}[^\\\\\\/<]+?))<\\/Data>"
      "(?i)<Data Name ='TargetFilename'>({file_path}({file_dir}(?:[^<]+)?[\\\\\\/])?({file_name}[^\\\\\\/<]+?(\\.({file_ext}[^\\\\\\/\\.<]+))))<\\/Data>"
      "(?i)<Provider Name ='({log_name}[^']+)'"
    ]
    DupFields = [
      "host->dest_host"
      "event_name->access"
    ]
  

}
```