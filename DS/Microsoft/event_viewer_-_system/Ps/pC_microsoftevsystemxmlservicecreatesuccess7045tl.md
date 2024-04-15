#### Parser Content
```Java
{
Name = "microsoft-evsystem-xml-service-create-success-7045-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - System"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      ">7045</eventid>"
      "<data name='accountname'"
    ]
    Fields = [
      "(?i)SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)ProcessID='({process_id}[^']+)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)>({event_code}\\d+)</EventID>"
      "(?i)<Security UserID='({user_sid}[^']+)"
      "(?i)<Data Name ='ServiceName'>({service_name}[^<]+?)\\s*</Data>"
      "(?i)<Data Name ='ServiceType'>({service_type}[^<]+?)\\s*</Data>"
      "(?i)<Data Name ='ImagePath'>({process_path}({process_dir}[^<>\\\"]*?[\\\\\\/]+)?({process_name}[^\\\"<>\\\\\\/]*))</Data>"
      "(?i)<Data Name ='ImagePath'>({process_command_line}\\\"({process_path}({process_dir}[^<>\\\"]*?[\\\\\\/]+)?({process_name}[^\\\"<>\\\\\\/]*))\\\"(\\s*({arg}[^<>]+))?)</Data>"
      "(?i)<Data Name ='AccountName'>(({account_domain}[^<>\\\\\\/]+)[\\\\\\/]+)?({account_name}[^<]+?)</Data>"
      "(?i)({event_name}A service was installed in the system)"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```