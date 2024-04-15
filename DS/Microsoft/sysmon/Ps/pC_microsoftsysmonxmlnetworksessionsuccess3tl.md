#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-network-session-success-3-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Sysmon"
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
    Conditions = [
      "<provider name='microsoft-windows-sysmon'"
      "<eventid>3</eventid>"
    ]
    Fields = [
      "(?i)<Provider Name ='Microsoft-Windows-Sysmon' Guid='\\{({process_guid}[^}]+?)\\}"
      "(?i)<EventID>({event_code}\\d+)<\\/EventID>"
      "(?i)<Task>({operation}.*?)<\\/Task>"
      "(?i)<Execution ProcessID='({process_id}\\d+)"
      "(?i)UtcTime:\\s*({time}\\d\\d\\d\\d-\\d\\d-\\d\\d \\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)"
      "(?i)<Computer>({host}.+?)<\\/Computer>"
      "(?i)<Security UserID='(({domain}[^\\\\]+)[\\\\\\/]+)?({user}.+?)'\\s*\\/>"
      "(?i)<EventData>.*?Image:\\s*({process_path}({process_dir}.*?)({process_name}[^.]+\\.exe))\\s*User:"
      "(?i)<EventData>.*?Image:\\s*({path}.+?)\\s*User:"
      "(?i)SourceIp:\\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)SourceHostname:\\s*({src_host}.*?)\\s*(Source|$)"
      "(?i)<EventData>.*?<Data Name ='UtcTime'>({time}\\d\\d\\d\\d-\\d\\d-\\d\\d \\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)"
      "(?i)<EventData>.*?<Data Name ='ProcessGuid'>\\{({process_guid}[^}]+)\\}<\\/Data>"
      "(?i)<EventData>.*?<Data Name ='ProcessId'>({process_id}\\d+)"
      "(?i)<EventData>.*?<Data Name ='Image'>({process_path}({process_dir}(?:[^<>]+)?[\\\\]+)?({process_name}[^\\\\<>]+))<\\/Data>"
      "(?i)<EventData>.*?<Data Name ='User'>(({domain}[^\\>]+?\\w+))?\\\\({user}[^\\<>]+)<\\/Data>"
      "(?i)<EventData>.*?<Data Name ='Protocol'>({protocol}[^<>]+)<\\/Data>"
      "(?i)<EventData>.*?<Data Name ='SourceIp'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)<EventData>.*?<Data Name ='SourceHostname'>({src_host}[^<>]+)</Data>"
      "(?i)<EventData>.*?<Data Name ='SourcePort'>({src_port}\\d+)"
      "(?i)<EventData>.*?<Data Name ='DestinationIp'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?"
      "(?i)<EventData>.*?<Data Name ='DestinationHostname'>({dest_host}[^<>]+)</Data>"
      "(?i)<EventData>.*?<Data Name ='DestinationPort'>({dest_port}\\d+)"
    ]
  

}
```