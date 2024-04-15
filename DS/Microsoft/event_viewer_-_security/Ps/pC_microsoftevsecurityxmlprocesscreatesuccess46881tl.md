#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-process-create-success-4688-1-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4688</eventid>"
      "a new process has been created"
      "creator subject:"
    ]
    Fields = [
      "(?i)({event_name}A new process has been created)"
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)<"
      "(?i)<EventID>({event_code}[^<]+)<"
      "(?i)Logon ID:\\s*(|-|({login_id}[^:]+?))\\s*Target Subject:"
      "(?i)Creator Subject:\\s*Security ID:\\s*(|-|({user_sid}[^:]+?))\\s*Account Name:"
      "(?i)Account Name:\\s*(|-|LOCAL SERVICE|({user}[^:]+?))\\s*Account Domain:"
      "(?i)Account Domain:\\s*(|-|NT AUTHORITY|({domain}[^:]+?))\\s*Logon ID:"
      "(?i)<Data Name ='SubjectUserSid'>({user_sid}[^<]+)<"
      "(?i)<Data Name ='SubjectUserName'>(LOCAL SERVICE|({user}[^<]+))<"
      "(?i)<Data Name ='SubjectDomainName'>(NT AUTHORITY|({domain}[^<]+))<"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+)<"
      "(?i)New Process ID:\\s*({process_guid}[x\\da-f]+)"
      "(?i)<Data Name ='NewProcessId'>\\s*({process_guid}[x\\da-f]+)<"
      "(?i)New Process Name:\\s*(|-|({process_path}({process_dir}(?:[^\"]+)?[\\\\\\/])?({process_name}[^\\\\\\/\\s]+)))\\s*Token Elevation Type:"
      "(?i)<Data Name ='NewProcessName'>\\s*(|-|({process_path}({process_dir}(?:[^\"]+)?[\\\\\\/])?({process_name}[^\\\\\\/\\s]+)))\\s*<\\/Data>"
      "(?i)New Process Name:\\s*(|-|({path}.+?))\\s*Token Elevation Type:"
      "(?i)<Data Name ='NewProcessName'>\\s*(|-|({path}.+?))\\s*<"
      "(?i)Process Command Line:\\s*(|-|({process_command_line}.+?))\\s*Token Elevation Type"
      "(?i)Process Command Line:\\s*(|-|(sc|((?:[^\"]+)?[\\\\\\/])?sc.exe)\\s*(?:\\\\*[\\w.\\-]+)?\\s*create\\s*({service_name}.+?))\\s+binPath= \\s*(|-|({process_path}({process_dir}(?:[^\"]+)?[\\\\\\/])?({process_name}[^\\\\\\/\\s]+)))\\s*Token Elevation Type"
      "(?i)<Data Name ='CommandLine'>\\s*(|-|({process_command_line}.+?))\\s*<"
      "(?i)Creator Process ID:\\s*({parent_process_guid}[x\\da-f]+)"
      "(?i)<Data Name ='ProcessId'>\\s*({parent_process_guid}[x\\da-f]+)<"
      "(?i)({operation_type}Process Creation)"
      "(?i)<Data Name ='ParentProcessName'>({parent_process}({parent_process_dir}[^<]+[\\\\\\/]+)?({parent_process_name}[^<]+))<"
    ]
    DupFields = [
      "host->dest_host"
      "process_guid->process_id"
    ]
  

}
```