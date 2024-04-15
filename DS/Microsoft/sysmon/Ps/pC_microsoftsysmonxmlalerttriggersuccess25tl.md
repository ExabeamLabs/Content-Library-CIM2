#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-alert-trigger-success-25-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Sysmon"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<provider name='microsoft-windows-sysmon'"
      "<eventid>25</eventid>"
      "<data name='image'>"
      "process tampering"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[\\w\\-.]+)"
      "(?i)<EventID>({event_code}25)"
      "(?i)ProcessID='({process_id}\\d+)'"
      "(?i)ThreadID='({thread_id}\\d+)'"
      "(?i)<Security UserID='({user_sid}[^']+)'"
      "(?i)Guid='\\{({process_guid}[^'}]+)"
      "(?i)({alert_name}Process Tampering)"
      "(?i)<Data Name ='Image'>({process_path}({process_dir}[^<>\"]*?[\\\\\\/]+)?({process_name}[^\"<>\\\\\\/]*))<\\/Data>"
    ]
    DupFields = [
      "host->dest_host"
    ]
  

}
```