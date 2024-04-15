#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-fail-4625-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4625</eventid>"
      "'failurereason'>"
    ]
    Fields = [
      "(?i)TimeCreated SystemTime(\\\\)?='({time}\\d+-\\d+-\\d+T\\d+:\\d+:\\d+)"
      "(?i)<Computer>({host}({dest_host}[\\w\\-]+)[^<]*)</Computer>"
      "(?i)<EventID>({event_code}\\d+)</EventID>"
      "(?i)<Data Name(\\\\)?='SubjectUserName'>(?=\\w)?(-|({src_user}[^<]+))<\\/Data>"
      "(?i)<Data Name(\\\\)?='SubjectDomainName'>((?=\\w))?(-|({src_domain}[^<]+))<\\/Data>"
      "(?i)<Data Name(\\\\)?='LogonType'>({login_type}\\d+)<\\/Data>"
      "(?i)<Data Name(\\\\)?='TargetUserSid'>({user_sid}[^<]+)</Data>"
      "(?i)<Data Name(\\\\)?='TargetUserName'>(?=\\w)(({email_address}[^@]+@[^.]+\\.[^<]+)|(({domain}[^\\<]+)\\+)?([^<]+\\.com|({user}[^<]+)))</Data>"
      "(?i)<Data Name(\\\\)?='TargetDomainName'>(?=\\w)({domain}[^<]+)</Data>"
      "(?i)<Data Name(\\\\)?='Status'>({result_code}[^<]+)</Data>"
      "(?i)<Data Name(\\\\)?='SubStatus'>({result_code}[^<]+)</Data>"
      "(?i)<Data Name(\\\\)?='IpAddress'>(?:-|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?)</Data>"
      "(?i)<Data Name(\\\\)?='LogonProcessName'>({auth_process}[^\\s<]+)"
      "(?i)<Data Name(\\\\)?='WorkstationName'>(-|({src_host_windows}[A-Za-z]+[\\w.-]+))\\s*</Data>"
      "(?i)<Data Name(\\\\)?='AuthenticationPackageName'>({auth_package}[^<]+)</Data>"
      "(?i)({event_name}An account failed to log on)"
      "(?i)<Data Name(\\\\)?='FailureReason'>({failure_reason}[^<]+)</Data>"
      "(?i)<Data Name =('|\")SubjectUserSid('|\")>({subject_sid}[^<]+)</Data>"
      "(?i)<Data Name =('|\")KeyLength('|\")>({key_length}\\d+)</Data>"
    ]
    DupFields = [
      "result_code->failure_code"
    ]
    ParserVersion = "v1.0.0"
  

}
```