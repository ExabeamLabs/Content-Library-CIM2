#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-file-permission-modify-4670-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>4670</eventid>"
      "<task>authorization policy change"
      "permissions on an object were changed"
    ]
    Fields = [
      "(?i)({event_name}Permissions on an object were changed)"
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z'\\/>"
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)Subject:.+?Security ID:\\s*({user_sid}[^\\s]+)"
      "(?i)Subject:.+?Account Name:\\s*(-|({user}[^\\s]+))"
      "(?i)Subject:.+?Account Domain:\\s*(-|({domain}[^\\s]+))"
      "(?i)Subject:.+?Logon ID:\\s*({login_id}[^\\s]+)"
      "(?i)Object:.+?Object Server:\\s*({object_server}[^\\s]+)"
      "(?i)Object:.+?Object Type:\\s*({object_type}[^\\s]+)"
      "(?i)Object:.+?Object Name:\\s*(-|({object_name}[^\\s]+))"
      "(?i)Process:.+?Process ID:\\s*({process_id}[^\\s]+)"
      "(?i)Process:.+?Process Name:\\s*({process_path}(?:({process_dir}.+?)[\\\\\\/]+)?({process_name}[^\\s\\\\\\/]+))\\s+Permissions Change:"
    ]
    DupFields = [
      "process_name -> file_name"
    ]
  

}
```