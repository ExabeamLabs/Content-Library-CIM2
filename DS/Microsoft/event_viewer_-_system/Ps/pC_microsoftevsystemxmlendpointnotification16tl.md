#### Parser Content
```Java
{
Name = "microsoft-evsystem-xml-endpoint-notification-16-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - System"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>16</eventid>"
      "<provider name='microsoft-windows-kernel-general'"
    ]
    Fields = [
      "(?i)<Computer>({host}[^<]+)<\\/Computer>"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)'"
      "(?i)<Message>\\s*({additional_info}[^<]+)<\\/Message>"
      "(?i)(<EventID)?>({event_code}\\d+)<\\/EventID>"
      "(?i)ProcessID='({process_id}\\d+)'"
      "(?i)Security UserID='({user_sid}[^']+)'"
      "(?i)<Data Name ='FailureReason'>({result_code}[^<]+)<\\/Data>"
      "(?i)Data Name ='SubjectDomainName'>({domain}[^<]+)<\\/Data>"
      "(?i)Data Name ='SubjectUserName'>({user}[^<]+)<\\/Data>"
      "(?i)Data Name ='Ipaddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?<\\/Data>"
      "(?i)Data Name ='SubjectLogonId'>({login_id}[^<]+)<\\/Data>"
    ]
  

}
```