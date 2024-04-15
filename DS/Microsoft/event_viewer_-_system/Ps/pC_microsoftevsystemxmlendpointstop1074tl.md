#### Parser Content
```Java
{
Name = "microsoft-evsystem-xml-endpoint-stop-1074-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - System"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
    Conditions = [
      "<system><provider"
      "<eventid qualifiers='"
      ">1074</eventid>"
      "<computer>"
      "shutdown type:"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)'/>"
      "(?i)<Computer>({host}({dest_host}[\\w\\-]+)[^<]*)</Computer>"
      "(?i)<Data Name ='param7'>(({domain}[^\\\\<]+?)\\\\)?({user}[^<]+)</Data>"
      "(?i)({event_code}1074)</EventID>"
      "(?i)<Message>The process [^<]+ has ({event_name}[^<]+?)\\s+[\\w\\-]+\\s+on behalf of user"
      "(?i)<Data Name ='param1'>({process_path}(({process_dir}[^\\.]+)?\\\\)?({process_name}[^<\\s]+)?)"
      "(?i)<Data Name ='param3'>({failure_reason}[^<]+)</Data>"
      "(?i)<Security UserID='({user_sid}[^<]+)'/>"
    ]
  

}
```