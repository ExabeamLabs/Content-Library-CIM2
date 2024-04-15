#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-process-create-success-processcreate-2-tl"
    Vendor = "Microsoft"
    Product = "Sysmon"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [
      "<provider name='microsoft-windows-sysmon'"
      "<eventid>10</eventid>"
      "<channel>microsoft-windows-sysmon/operational</channel>"
      "<data name="
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)"
      "(?i)<Data Name ='UtcTime'>({time}\\d\\d\\d\\d-\\d\\d-\\d\\d \\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)</Data>"
      "(?i)<Computer>({host}({dest_host}[\\w\\-]+)[^<]*)</Computer>"
      "(?i)<Data Name ='User'>(({domain}[^\\\\<]+?)\\\\)?({user}[^<]+)</Data>"
      "(?i)<Security UserID='({user_sid}[^']+)'/>"
      "(?i)<Data Name ='Hashes'>.*?MD5=({hash_md5}[A-F0-9a-f]+).*?</Data>"
      "(?i)(?i)<Data Name ='SourceProcessGuid'>\\{({process_guid}[A-F0-9a-f-]+)\\}</Data>"
      "(?i)<Data Name ='SourceProcessId'>({process_id}\\d+)</Data>"
      "(?i)(?i)<Data Name ='TargetProcessGuid'>\\{({dest_process_id}[A-F0-9a-f-]+)\\}</Data>"
      "(?i)<Data Name ='TargetProcessId'>({dest_process_id}\\d+)</Data>"
      "(?i)<Data Name ='CommandLine'>({process_command_line}[^<]+?)\\s*</Data>"
      "(?i)<Data Name ='SourceImage'>({parent_process}(({parent_process_dir}[^<]*)\\\\+)?({parent_process_name}[^<]+?))</Data>"
      "(?i)<Data Name ='TargetImage'>({process_path}(({process_dir}[^<]*)\\\\+)?({process_name}[^<]+?))</Data>"
      "(?i)<Data Name ='GrantedAccess'>({result}[^<]+)</Data>"
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)CallTrace:\\s*({additional_info}[^<]+)</Message>"
    ]
    DupFields = [
      "host->src_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```