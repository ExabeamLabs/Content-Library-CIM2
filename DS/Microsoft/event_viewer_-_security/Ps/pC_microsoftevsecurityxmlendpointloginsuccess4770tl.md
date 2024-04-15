#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-success-4770-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4770</eventid>"
      "<data name='ipaddress'>"
    ]
    Fields = [
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)<Data Name ='TargetSid'>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"
      "(?i)<Data Name ='TargetUserName'>(?=\\w)({user}[^<@\\s]+)</Data>"
      "(?i)<Data Name ='TargetUserName'>(?=\\w)({user}[^@<]+)@({domain}[^<]+)</Data>"
      "(?i)<Data Name ='TargetDomainName'>(?=\\w)({domain}[^<]+)</Data>"
      "(?i)<Data Name ='IpAddress'>(::\\w+:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?</Data>"
      "(?i)<Data Name ='ServiceName'>({service_name}[^<]+)</Data>"
      "(?i)<Data Name ='ServiceName'>({dest_host}[^<]+\\$)</Data>"
      "(?i)<Data Name ='TicketOptions'>({ticket_options}[^<]+)</Data>"
      "(?i)<Data Name ='TicketEncryptionType'>({ticket_encryption_type}[^<]+)</Data>"
    ]
    ParserVersion = "v1.0.0"
  

}
```