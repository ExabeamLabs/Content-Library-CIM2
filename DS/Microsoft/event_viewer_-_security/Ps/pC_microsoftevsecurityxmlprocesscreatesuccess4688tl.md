#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-process-create-success-4688-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4688</eventid>"
      "'subjectusersid'>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)({event_name}A new process has been created)"
      "(?i)<Computer>({host}[^<]+)<"
      "(?i)({event_code}4688)"
      "(?i)<Data Name ='SubjectUserSid'>({user_sid}[^<]+?)<"
      "(?i)<Data Name ='SubjectUserName'>(-|LOCAL SERVICE|({full_name}[^<\\s]+\\s[^<]+)|({user}[^<]+?))<"
      "(?i)<Data Name ='SubjectDomainName'>(-|NT AUTHORITY|({domain}[^<]+?))<"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+?)<"
      "(?i)<Data Name ='NewProcessId'>({process_guid}[x\\da-f]+)<"
      "(?i)<Data Name ='NewProcessName'>({process_path}({process_dir}(?:[^<>]+)?[\\\\\\/])?({process_name}[^\\\\\\/<>]+))<"
      "(?i)<Data Name ='CommandLine'>\"?\\s*({process_command_line}[^<]+?)\\s*\"?<"
      "(?i)<Data Name ='CommandLine'>\\s*(|-|(sc|((?:[^\"]+)?[\\\\\\/])?sc.exe)\\s*(?:\\\\*[\\w.\\-]+)?\\s*create\\s*({service_name}.+?))\\s+binPath= ({process_path}({process_dir}(?:[^<>]+)?[\\\\\\/])?({process_name}[^\\\\\\/<>]+))<"
      "(?i)<Data Name ='ProcessId'>({parent_process_guid}[x\\da-f]+)<"
      "(?i)<Data Name ='ParentProcessName'>({parent_process}({parent_process_dir}[^<]+[\\\\\\/]+)?({parent_process_name}[^<]+))<\\/Data>"
    ]
    DupFields = [
      "host->dest_host"
      "process_guid->process_id"
    ]
  

}
```