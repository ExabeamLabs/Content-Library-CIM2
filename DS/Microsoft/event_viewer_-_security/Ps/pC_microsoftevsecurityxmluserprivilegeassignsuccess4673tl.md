#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-privilege-assign-success-4673-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4673</eventid>"
      "a privileged service was called"
      "privileges:"
    ]
    Fields = [
      "(?i)({event_name}A privileged service was called)"
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)({result}Information|Audit Success|Success Audit|Failure Audit|Audit Failure)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)Process Name:\\s*(?: |({process_path}({process_dir}(?:[^\"]+?)?[\\\\\\/])?({process_name}[^\\\\\\/\"]+?)))\\s*Service Request Information:"
      "(?i)Account Name:\\s*({user}[^=]+?)\\s*Account Domain:"
      "(?i)Account Domain:\\s*({domain}[^=]+?)\\s*Logon ID:"
      "(?i)Logon ID:\\s*({login_id}.+?)\\s*Service:"
      "(?i)Server:\\s*({object_server}[^=]+?)\\s*Service Name"
      "(?i)Privileges:\\s*({privileges}[^<>\\s\"=]+)"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```