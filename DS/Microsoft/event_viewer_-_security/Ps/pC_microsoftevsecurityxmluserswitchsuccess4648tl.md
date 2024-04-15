#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-switch-success-4648-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4648</eventid>"
      "='processname'"
    ]
    Fields = [
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<EventID>({event_code}\\d+)</EventID>"
      "(?i)<Data Name ='SubjectUserSid'>({user_sid}[^<]+)<\\/Data>"
      "(?i)<Data Name ='SubjectUserName'>(-|({user}[^<]+))</Data>"
      "(?i)<Data Name ='SubjectDomainName'>(-|({domain}[^<]+))</Data>"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+)</Data>"
      "(?i)<Data Name ='TargetUserName'>({dest_user}[^<]+?)\\s*</Data>"
      "(?i)<Data Name ='TargetDomainName'>({dest_domain}[^<]+)</Data>"
      "(?i)<Data Name ='TargetServerName'>({dest_host}[\\w\\-]+)[^<]*</Data>"
      "(?i)<Data Name ='ProcessId'>({process_id}[^<]+)</Data>"
      "(?i)<Data Name ='ProcessName'>({process_path}({process_dir}(?:[^<]+)?[\\\\\\/])?({process_name}[^\\\\\\/\\\"]+?))<\\/Data>"
      "(?i)<Data Name ='IpAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?</Data>"
      "(?i)<Data Name ='TargetInfo'>({dest_service_name}[^<]+)</Data>"
      "(?i)<Message>({event_name}A logon was attempted using explicit credentials)"
    ]
  

}
```