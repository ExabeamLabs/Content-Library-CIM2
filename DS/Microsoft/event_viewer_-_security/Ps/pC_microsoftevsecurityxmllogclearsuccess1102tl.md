#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-log-clear-success-1102-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "the audit log was cleared"
      "<eventid>1102"
    ]
    Fields = [
      "(?i)EventTime\":\"({time}\\d\\d\\d\\d-\\d\\d-\\d\\d \\d\\d:\\d\\d:\\d\\d)\""
      "(?i)Hostname\":\"({host}[^\"]+)\""
      "(?i)({event_code}1102)"
      "(?i)({event_name}The audit log was cleared)"
      "(?i)<Message>Process '?({process_name}[^\\s']+)"
      "(?i)<Security UserID(\\\\)?='({user_sid}[^']+)"
      "(?i)<Execution ProcessID(\\\\)?='({process_id}[^']+)"
      "(?i)<EventID[^<]*?>({event_code}\\d+)"
      "(?i)<Keyword>(Classic|({result}[^<]+))</Keyword>"
      "(?i)<Data Name(\\\\)?='ProcessName'>({process_path}({process_dir}[^<>]*?[\\\\\\/]+)?({process_name}[^<>\\\\\\/]+))</Data>"
      "(?i)<Data Name ='TargetProcessName'>({dest_process_path}({dest_process_dir}[^<>]*?[\\\\\\/]+)?({dest_process_name}[^<>\\\\\\/]+))</Data>"
      "(?i)<Data Name(\\\\)?='ProcessId'>({process_id}[^<]+?)\\s*</Data>"
      "(?i)Security ID:\\s*({user_sid}\\S+)\\s+Account Name:"
      "(?i)Account Name:\\s*(LOCAL SERVICE|-|({user}\\S+))\\s+Account Domain:"
      "(?i)Account Domain:\\s*(NT AUTHORITY|-|({domain}\\S+))\\s+Logon ID:"
      "(?i)Client IP: ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)ThreadID(\\\\)?='({thread_id}\\d+)"
      "(?i)\\s+Account Name:\\s+({user}[^:]+?)\\s+Domain"
      "(?i)\\s+Domain Name:\\s+({domain}[^\\s]+)"
      "(?i)\\s+Logon ID:\\s+({login_id}[^\\s]+)"
      "(?i)SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d.\\d\\d\\d\\d\\d\\d\\d\\d\\dZ)"
      "(?i)\\s+Logon ID:\\s+({login_id}[^<>\\s=]+)"
      "(?i)<Computer>({host}[^<]+?)<\\/Computer>"
      "(?i)<Computer>(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?|({src_host}[\\w\\-.]+))<\\/Computer>"
      "(?i)Security ID:\\s*({user_sid}[^\\s:]+)"
    ]
  

}
```