#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-handle-request-success-4659-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>4659</eventid>"
      "open object with delete intent"
      "netapp-security-auditing"
    ]
    Fields = [
      "(?i)TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)"
      "(?i)({event_name}Open Object with Delete Intent)"
      "(?i)<EventID>({event_code}4659)<\\/EventID>"
      "(?i)<Result>({action}[^<]+)<\\/Result>"
      "(?i)<Computer>([^\\/]+\\/)?({host}[^<]+)<\\/Computer>"
      "(?i)<Data Name ='SubjectIP'[^>]+>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?<\\/Data>"
      "(?i)<Data Name ='SubjectUserSid'>({user_sid}[^<]+)<\\/Data>"
      "(?i)<Data Name ='SubjectDomainName'>({domain}[^<]+)<\\/Data>"
      "(?i)<Data Name ='SubjectUserName'>({user}[^<]+)<\\/Data>"
      "(?i)<Data Name ='ObjectServer'>({object_server}[^<]+)<\\/Data>"
      "(?i)<Data Name ='ObjectType'>({object_class}[^<]+)<\\/Data>"
      "(?i)<Data Name ='ObjectName'>({object}[^<]+)<\\/Data>"
      "(?i)<Data Name ='ObjectName'>({file_path}({file_dir}[^<]+)\\/({file_name}[^<]+\\.({file_ext}[^<]+)))<\\/Data>"
      "(?i)<Data Name ='DesiredAccess'>({access}[^<]+?)\\s*<\\/Data>"
      "(?i)<Data Name ='HandleID'>({object_id}[^<]+)<\\/Data>"
    ]
  

}
```