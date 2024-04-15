#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-process-create-success-processcreate-tl"
    Vendor = "Microsoft"
    Product = "Sysmon"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [
      "<provider name='microsoft-windows-sysmon'"
      "<eventid>1</eventid>"
      "<channel>microsoft-windows-sysmon/operational</channel>"
      "<data name="
    ]
    Fields = [
      "(?i)<Data Name ='UtcTime'>({time}\\d\\d\\d\\d-\\d\\d-\\d\\d \\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)</Data>"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)"
      "(?i)<Computer>({host}[^<]+?)</Computer>"
      "(?i)<Data Name ='User'>((NT AUTHORITY|NT-AUTORITÄT|({domain}[^\\\\<]+?))\\\\)?(SYSTEM|(NETWORK|LOCAL) SERVICE|({user}[^<]+?))</Data>"
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)<Security UserID='({user_sid}[^>]+?)'/>"
      "(?i)<Data Name ='LogonId'>({login_id}[^<]+?)</Data>"
      "(?i)<Data Name ='Hashes'>[^=]*?MD5=({hash_md5}[A-F0-9a-f]+)[^<]*?<\\/Data>"
      "(?i)<Data Name ='ProcessGuid'>\\{({process_guid}[A-F0-9a-f-]+)\\}</Data>"
      "(?i)<Data Name ='ProcessId'>({process_id}\\d+)</Data>"
      "(?i)<Data Name ='ParentProcessGuid'>\\{({parent_process_guid}[A-F0-9a-f-]+)\\}</Data>"
      "(?i)<Data Name ='CommandLine'>\"?\\s*({process_command_line}[^<]+?)\\s*</Data>"
      "(?i)<Data Name ='Image'>(({process_dir}[^<]+)\\\\)?({process_name}[^<]+?)</Data>"
      "(?i)<Data Name ='Image'>({process_path}[^<]+?)</Data>"
      "(?i)<Data Name ='ParentImage'>({parent_process}(({parent_process_dir}[^<]+)\\\\)?({parent_process_name}[^<]+?))<\\/Data>"
    ]
    DupFields = [
      "host->src_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```