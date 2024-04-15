#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-process-create-success-1-tl"
    Vendor = "Microsoft"
    Product = "Sysmon"
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
    Conditions = [
      "<provider name='microsoft-windows-sysmon'"
      "<eventid>1</eventid>"
    ]
    Fields = [
      "(?i)<Provider Name ='Microsoft-Windows-Sysmon' Guid='\\{({process_guid}[^}]+?)\\}"
      "(?i)<EventID>({event_code}\\d+)</EventID>"
      "(?i)<Task>({operation}.*?)</Task>"
      "(?i)<Execution ProcessID='({process_id}\\d+)"
      "(?i)UtcTime:\\s*({time}\\d\\d\\d\\d-\\d\\d-\\d\\d \\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)"
      "(?i)<Computer>({host}.+?)</Computer>"
      "(?i)<Security UserID='(({domain}[^\\\\>]+?)\\\\)?({user}.+?)'\\s*/>"
      "(?i)<EventData>.*?Image:\\s*({process_path}({process_dir}.*?)({process_name}[^.\\\\]+\\.exe))\\s*CommandLine:"
      "(?i)<EventData>.*?Image:\\s*({path}.+?)\\s*CommandLine:"
      "(?i)CommandLine:\\s*({process_command_line}.*?)\\s*CurrentDirectory:"
      "(?i),MD5=({hash_md5}[^,]+)(,|\\s*$)"
    ]
    DupFields = [
      "host->src_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```