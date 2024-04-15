#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-notification-5031-tl"
    Vendor = "Microsoft"
    ParserVersion = "v1.0.0"
    Product = "Event Viewer - System"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>5031<"
      "windows firewall blocked an application from accepting incoming connections on the network"
    ]
    Fields = [
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)({event_name}Windows Firewall blocked an application from accepting incoming connections on the network.)"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Execution ProcessID='({process_id}\\d+)' ThreadID='({thread_id}\\d+)'"
      "(?i)<Data Name ='Application'>({process_path}({process_dir}(?:[^<]+)?[\\\\\\/])?({process_name}[^\\\\\\/]+?))<\\/Data>"
    ]
  

}
```