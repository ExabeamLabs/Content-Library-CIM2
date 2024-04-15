#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-process-pipe-create-17-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Sysmon"
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
    Conditions = [
      "<eventid>17<"
      "createpipe"
      "pipe created:"
      "pipename:"
    ]
    Fields = [
      "(?i)<Data Name ='UtcTime'>({time}\\d\\d\\d\\d-\\d\\d-\\d\\d\\s\\d\\d:\\d\\d:\\d\\d\\.\\d+)<\\/Data>"
      "(?i)<Computer>({host}[^<]+)<\\/Computer>"
      "(?i)<EventID>({event_code}\\d+)<\\/EventID>"
      "(?i)<Data Name ='ProcessId'>({process_id}\\d+)<\\/Data>"
      "(?i)<Data Name ='Image'>({process_path}(({process_dir}[^<>]+?)[\\\\\\/]+)?({process_name}[^\\\\\\/<>]+?)?)<\\/Data>"
      "(?i)<Data Name ='ProcessGuid'>({process_guid}[^<]+)<\\/Data>"
      "(?i)<Data Name ='EventType'>({event_name}[^<]+)<\\/Data>"
      "(?i)<Security UserID='({user_sid}[^']+)'"
      "(?i)({log_name}Microsoft-Windows-Sysmon)"
    ]
  

}
```