#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-notification-6417-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>6417<"
      "the fips mode crypto selftests succeeded"
    ]
    Fields = [
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)({event_name}The FIPS mode crypto selftests succeeded.)"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Execution ProcessID='({process_id}\\d+)' ThreadID='({thread_id}\\d+)'"
      "(?i)<Data Name[^<>]+?ProcessName[^<>]+?>(-|({process_path}({process_dir}[^<>]*?[\\\\\\/]+)?({process_name}[^<>\\\\\\/]+)))</Data>"
    ]
  

}
```