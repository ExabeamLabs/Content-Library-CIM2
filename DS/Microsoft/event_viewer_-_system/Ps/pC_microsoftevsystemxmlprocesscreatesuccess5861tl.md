#### Parser Content
```Java
{
Name = "microsoft-evsystem-xml-process-create-success-5861-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - System"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>5861"
      "microsoft-windows-wmi-activity"
    ]
    Fields = [
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<Security UserID='({user_sid}[^']+)"
      "(?i)({process_name}WMI)"
      "(?i)Query\\s*=\\s*\"*({process_command_line}[^\";]+)"
      "(?i)Consumer:\\s* instance of\\s*({process_name}.+?)\\s*\\{"
    ]
    DupFields = [
      "host->dest_host"
    ]
  

}
```