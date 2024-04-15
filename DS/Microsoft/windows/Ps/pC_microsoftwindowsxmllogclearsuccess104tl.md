#### Parser Content
```Java
{
Name = "microsoft-windows-xml-log-clear-success-104-tl"
    Vendor = "Microsoft"
    Product = "Windows"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>104<"
      "log file was cleared."
    ]
    Fields = [
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)<Keywords>({result}[^<]+)"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Computer>(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?|({src_host}[\\w\\-\\.]+))"
      "(?i)<Security UserID='({user_sid}[^'<\\/]+)"
      "(?i)<SubjectUserName>(SYSTEM|({user}[^<]+))"
      "(?i)<SubjectDomainName>(NT AUTHORITY|({domain}[^<]+))"
      "(?i)<Message>({event_name}[^<]+)"
      "(?i)<Level>({alert_severity}[^<]+)"
    ]
    ParserVersion = "v1.0.0"
  

}
```