#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-service-create-success-4697-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4697</eventid>"
      "'servicefilename'>"
    ]
    Fields = [
      "(?i)SystemTime(\\\\)?=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)<Data Name(\\\\)?='SubjectUserSid'>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"
      "(?i)<Data Name(\\\\)?='SubjectUserName'>(?=\\w)({user}[^<]+)</Data>"
      "(?i)<Data Name(\\\\)?='SubjectDomainName'>(?=\\w)({domain}[^<]+)</Data>"
      "(?i)<Data Name(\\\\)?='SubjectLogonId'>(?=\\w)({login_id}[^<]+)</Data>"
      "(?i)<Data Name(\\\\)?='ServiceName'>(?=\\w)(({service_name}[^_]+?)(_[^\\<]+)?)</Data>"
      "(?i)<Data Name(\\\\)?='ServiceAccount'>(?=\\w)(({account_domain}[^\\\\<]*)\\\\)?({account_name}[^<]+)</Data>"
      "(?i)<Data Name(\\\\)?='ServiceFileName'>\\\"?(?=\\w)({process_path}({process_dir}(?:(\\w+:)?[^:<\\\"]+)?[\\\\])?({process_name}[^<\\\"\\s]+))"
      "(?i)<Data Name(\\\\)?='ServiceType'>(?=\\w)({service_type}[^<]+)</Data>"
      "(?i)<Message>({event_name}A service was installed in the system)"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```