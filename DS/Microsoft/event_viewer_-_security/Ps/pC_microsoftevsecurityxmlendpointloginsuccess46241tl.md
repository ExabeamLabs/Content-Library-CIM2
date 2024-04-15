#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-success-4624-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4624</eventid>"
      "<data name=\"logontype\""
    ]
    Fields = [
      "(?i)SystemTime=\"({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)({event_name}An account was successfully logged on)"
      "(?i)<Computer>([^<>]+?[\\\\\\/]+)?({host}({dest_host}[\\w\\-]+)[^<]*)<"
      "(?i)<EventID>({event_code}[^<]+)<"
      "(?i)<Data Name =\"LogonType\">({login_type}\\d+)<"
      "(?i)<Data Name =\"TargetUserName\">({user}[^<]+)<"
      "(?i)<Data Name =\"TargetDomainName\">(-|({domain}[^<]+))<"
      "(?i)<Data Name =\"ProcessName\">(?:-|({process_path}({process_dir}[^<>]*?[\\\\\\/]+)?({process_name}[^<>\\\\\\/]+)))<"
      "(?i)<Data Name =\"IpAddress\"[^<>]*?>(?:-|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?)<"
      "(?i)<Data Name =\"LogonProcessName\">({auth_process}[^\\s<]+)"
      "(?i)<Data Name =\"AuthenticationPackageName\">({auth_package}[^<]+)<"
      "(?i)<Data Name =\"TargetLogonId\">({login_id}[^<]+)<"
      "(?i)<Data Name =\"TargetUserSid\">({user_sid}[^<]+)<"
      "(?i)<Data Name =\"WorkstationName\">([A-Fa-f:\\d.]+|-|({src_host_windows}[^<]+?))\\s*<"
      "(?i)EventRecordID>({event_id}[^<]+)<"
      "(?i)<Data Name =\"SubjectUserSid\">({subject_sid}[^<]+)<"
      "(?i)<Data Name =\"KeyLength\">({key_length}\\d+)<"
    ]
    ParserVersion = "v1.0.0"
  

}
```