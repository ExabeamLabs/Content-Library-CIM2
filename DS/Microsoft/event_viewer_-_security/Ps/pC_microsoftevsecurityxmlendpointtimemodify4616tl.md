#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-time-modify-4616-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "the system time was changed"
      "<eventid>4616<"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime(\\\\)?='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)"
      "(?i)<Computer>({host}[^<>]+)<"
      "(?i)<Message>({event_name}[^:<\\.]+)"
      "(?i)<Message>({event_name}[^<]+?)\\.(\\s|<)"
      "(?i)<Message>({additional_info}[^<]+?)\\s*<"
      "(?i)<Message>Process '?({process_name}[^\\s']+)"
      "(?i)<Security UserID(\\\\)?='({user_sid}[^']+)"
      "(?i)<Execution ProcessID(\\\\)?='({process_id}[^']+)"
      "(?i)<EventID[^<]*?>({event_code}\\d+)"
      "(?i)<Keyword>({result}[^<]+)<"
      "(?i)<Data Name(\\\\)?='ProcessName'>({process_path}({process_dir}[^<>]*?[\\\\\\/]+)?({process_name}[^<>\\\\\\/]+))</Data>"
      "(?i)<Data Name ='TargetProcessName'>({dest_process_path}({dest_process_dir}[^<>]*?[\\\\\\/]+)?({dest_process_name}[^<>\\\\\\/]+))</Data>"
      "(?i)<Data Name(\\\\)?='ProcessId'>({process_id}[^<]+?)\\s*<"
      "(?i)Security ID:\\s*({user_sid}\\S+)\\s+Account Name:"
      "(?i)Account Name:\\s*(LOCAL SERVICE|-|({user}\\S+))\\s+Account Domain:"
      "(?i)Account Domain:\\s*(NT AUTHORITY|-|({domain}\\S+))\\s+Logon ID:"
      "(?i)Logon ID:\\s*({login_id}\\S+)\\s+"
      "(?i)Task Name:\\s*(|-|({task_name}[^:]+?))\\s*Task Content:"
      "(?i)Client IP: ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)ThreadID(\\\\)?='({thread_id}\\d+)"
    ]
  

}
```