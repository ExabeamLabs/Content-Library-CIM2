#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-4769-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4769</eventid>"
      "<data name='servicename'>"
    ]
    Fields = [
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)({event_name}A Kerberos service ticket was requested)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)<Data Name ='Status'>({result_code}[^<]+)</Data>"
      "(?i)<Data Name ='ServiceName'>({dest_host}[\\w-]+)\\$</Data>"
      "(?i)<Data Name ='ServiceName'>({service_name}[^<]+)</Data>"
      "(?i)<Data Name ='TicketOptions'>({ticket_options}[^<]+)</Data>"
      "(?i)<Data Name ='TicketEncryptionType'>({ticket_encryption_type}[^<]+)</Data>"
      "(?i)<Data Name ='TargetUserName'>(([^\/<@]+\/+)({src_host}[^<@]+)(@({domain}[^<]+))?|(?=\\w)({user}[^<@\\s]+)(@({=domain}[^<@\\s]+?))?)<\/Data>"
      "(?i)<Data Name ='TargetDomainName'>(?=\\w)({domain}[^<]+)</Data>"
      "(?i)<Data Name ='IpAddress'>(::1|(::[\\w]+:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?)</Data>"
    ]
    DupFields = [
      "result_code->failure_code"
    ]
    ParserVersion = "v1.0.0"
  

}
```