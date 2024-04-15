#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-file-permission-modify-4670-2-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>4670</eventid>"
      "<data name='subjectusername'>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d{3})"
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)<Data Name ='ObjectServer'>(-|({object_server}[^<]+))</Data>"
      "(?i)<Data Name ='ObjectType'>(-|({object_type}[^<]+))</Data>"
      "(?i)<Data Name ='ObjectName'>(-|({object_name}[^<]+))</Data>"
      "(?i)<Data Name ='ProcessId'>(-|({process_id}[^<]+))</Data>"
      "(?i)<Data Name ='SubjectUserSid'>(-|({user_sid}[^<]+))</Data>"
      "(?i)<Data Name ='SubjectUserName'>(-|({user}[^<]+))</Data>"
      "(?i)<Data Name ='SubjectDomainName'>(-|({domain}[^<]+))</Data>"
      "(?i)<Data Name ='SubjectLogonId'>(-|({login_id}[^<]+))</Data>"
      "(?i)<Data Name ='ProcessName'>(-|({process_path}(({process_dir}[^<>]+?)[\\\\\\/]+)?({process_name}[^\\\\\\/<>]+?)))</Data>"
    ]
    DupFields = [
      "process_name -> file_name"
    ]
  

}
```