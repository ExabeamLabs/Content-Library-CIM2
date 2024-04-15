#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-scheduled-task-create-success-4698-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4698</eventid>"
      "'taskname'>"
    ]
    Fields = [
      "(?i)SystemTime(\\\\)?=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)<Data Name(\\\\)?='SubjectUserSid'>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"
      "(?i)<Data Name(\\\\)?='SubjectUserName'>(?=\\w)({user}[^<]+)</Data>"
      "(?i)<Data Name(\\\\)?='SubjectDomainName'>(?=\\w)({domain}[^<]+)</Data>"
      "(?i)<Data Name(\\\\)?='SubjectLogonId'>(?=\\w)({login_id}[^<]+)</Data>"
      "(?i)<Data Name(\\\\)?='TaskName'>(?=[\\\\\\w])({task_name}[^<]+)</Data>"
      "(?i)<UserId>(?=\\w)(({account_domain}[^\\\\<]*)\\\\)?({account_name}[^<]+)</UserId>"
      "(?i)<Settings>\\s*({additional_info}.+?)\\s*</Settings>"
      "(?i)<Triggers>\\s*({triggers}.+?)\\s*</Triggers>"
      "(?i)<RunLevel>(?=\\w)({run_level}[^<]+)</RunLevel>"
      "(?i)<LogonType>(?=\\w)({login_type_text}[^<]+)</LogonType>"
      "(?i)<RegistrationInfo>.+?<Author>(?=\\w)({author}[^<]+)</Author>"
      "(?i)<RegistrationInfo>.+?<Description>(?=\\w)({description}[^<]+)</Description>"
      "(?i)<Command>\\\"?({process_path}({process_dir}(?:(\\w+:)?[^:<\\\"]+)?[\\\\\\/])?({process_name}[^<\\\"]+))"
      "(?i)<Arguments>(\\\"+)?({arg}[^<\\\"]+)"
      "(?i)<Message>({event_name}A scheduled task was created)"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```