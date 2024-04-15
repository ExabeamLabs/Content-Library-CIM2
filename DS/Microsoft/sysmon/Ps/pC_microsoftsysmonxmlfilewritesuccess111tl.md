#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-file-write-success-11-1-tl"
    Vendor = "Microsoft"
    Product = "Sysmon"
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
    Conditions = [
      "<provider name='microsoft-windows-sysmon'"
      "logrhythm:"
      "<eventid>11</eventid>"
    ]
    Fields = [
      "(?i)<Provider Name ='Microsoft-Windows-Sysmon' Guid='\\{({process_guid}[^}]+?)\\}"
      "(?i)<EventID>({event_code}\\d+)</EventID>"
      "(?i)<Task>({operation}.*?)</Task>"
      "(?i)<Execution ProcessID='({process_id}\\d+)"
      "(?i)created:UtcTime:\\s*({time}\\d\\d\\d\\d-\\d\\d-\\d\\d \\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)"
      "(?i)<Computer>({host}.+?)</Computer>"
      "(?i)<Security UserID='(({domain}[^\\\\>]+?)\\\\)?({user}.+?)'\\s*/>"
      "(?i)<EventData>.*?Image:\\s*({process_path}({process_dir}.*?)({process_name}[^.\\\\]+\\.exe))\\s*TargetFilename:"
      "(?i)<EventData>.*?Image:\\s*({path}.+?)\\s*TargetFilename:"
      "(?i)TargetFilename:\\s*({file_path}({file_dir}.*?)({file_name}[^\\\\.]+(\\.({file_ext}[^\\\\.]+?))?))\\s*CreationUtcTime:"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```