#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-registry-create-success-4657-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>4657</eventid>"
      "<eventrecordid>"
    ]
    Fields = [
      "(?i)<EventID>({event_code}\\d+)</EventID>"
      "(?i)<Keywords>({result}[^\\<]+)</Keywords>"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)'"
      "(?i)<EventRecordID>({event_id}[^\\<]+)</EventRecordID>"
      "(?i)<Computer>({host}[^\\<]+)</Computer>"
      "(?i)<Data Name ='SubjectUserSid'>({user_sid}[^\\<]+)</Data>"
      "(?i)<Data Name ='SubjectUserName'>({user}[^\\<]+)</Data>"
      "(?i)<Data Name ='SubjectDomainName'>({domain}[^\\<]+)</Data>"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^\\<]+)</Data>"
      "(?i)<Data Name ='HandleId'>({object_id}[^\\<]+)</Data>"
      "(?i)<Data Name ='OperationType'>({operation}[^\\<]+)</Data>"
      "(?i)<Data Name ='NewValueType'>(-|({registry_details_type}[^\\<]+))</Data>"
      "(?i)<Data Name ='NewValue'>(-|({registry_details}[^\\<]+))</Data>"
      "(?i)<Data Name ='ProcessId'>({process_id}[^\\<]+)</Data>"
      "(?i)<Data Name ='ProcessName'>({process_path}({process_dir}(?:(\\w+:)?[^:]+)?[\\\\\\/])?({process_name}.+?))</Data>"
      "(?i)<Data Name ='ObjectName'>({registry_key}[^\\<]+)<\\/Data>"
      "(?i)<Data Name ='ObjectValueName'>({registry_value}[^\\<]+)<\\/Data>"
    ]
  

}
```