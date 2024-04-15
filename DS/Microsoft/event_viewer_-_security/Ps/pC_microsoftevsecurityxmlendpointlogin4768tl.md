#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-4768-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4768</eventid>"
      "<data name='targetsid'>"
    ]
    Fields = [
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)({event_name}A Kerberos authentication ticket \\(TGT\\) was requested)"
      "(?i)<Computer>({host}[\\w.-]+)</Computer>"
      "(?i)<EventID>({event_code}\\d+)</EventID>"
      "(?i)<Data Name ='TargetSid'>(NULL SID|({user_sid}[^<]+))</Data>"
      "(?i)<Data Name ='Status'>({result_code}[^<]+)</Data>"
      "(?i)<Data Name ='TargetUserName'>(?=\\w)({user}[^<=@]+)(@({domain}[^@<=]+))?</Data>"
      "(?i)<Data Name ='TargetDomainName'>(?=\\w)({domain}[^<]+)</Data>"
      "(?i)<Data Name ='IpAddress'>(::[\\w]+:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?</Data>"
      "(?i)<Data Name ='TicketEncryptionType'>({ticket_encryption_type}[^<]+)</Data>"
      "(?i)<Data Name ='TicketOptions'>({ticket_options}[^<]+)</Data>"
      "(?i)<Data Name ='ServiceName'>({service_name}[^\/\\<]+)</Data>"
    ]
    DupFields = ["host->dest_host"]
    ParserVersion = "v1.0.0"
  

}
```