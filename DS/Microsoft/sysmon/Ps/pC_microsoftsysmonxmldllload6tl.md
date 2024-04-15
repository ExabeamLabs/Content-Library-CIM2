#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-dll-load-6-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Sysmon"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>6</eventid>"
      "<eventrecordid>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z'\\/>"
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)({event_name}Driver loaded)"
      "(?i)<Keywords>({result}[^<]+)</Keywords>"
      "(?i)<EventRecordID>({event_id}[^<]+)<\\/EventRecordID>"
      "(?i)<Security UserID='({user_sid}.+?)'\\/>"
      "(?i)<Data Name ='ImageLoaded'>({file_path}({file_dir}(?:[^<]+)?[\\\\\\/])?({file_name}[^\\\\\\/<]+?(\\.({file_ext}[^\\\\\\/\\.<]+))))<\\/Data>"
      "(?i)<Data Name ='Hashes'>[^<>]*?MD5=({hash_md5}[^,<]+)"
      "(?i)({log_name}Microsoft-Windows-Sysmon)"
    ]
    DupFields = [
      "host->dest_host"
      "event_name->operation"
    ]
  

}
```