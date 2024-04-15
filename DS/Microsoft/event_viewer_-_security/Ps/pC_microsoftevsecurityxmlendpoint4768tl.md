#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-4768-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "\"eventid\":\"4768\""
      "<data name='"
    ]
    Fields = [
      "(?i)\"TimeGenerated\":\"({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)\"Computer\":\"({host}[^\"]+)"
      "(?i)\"EventID\":\"({event_code}\\d+)"
      "(?i)<Data Name ='TargetSid'>({user_sid}[^<]+)</Data>"
      "(?i)<Data Name ='Status'>({result_code}[^<]+)</Data>"
      "(?i)<Data Name ='TargetUserName'>(?=\\w)({user}[^<]+)</Data>"
      "(?i)<Data Name ='TargetDomainName'>(?=\\w)({domain}[^<]+)</Data>"
      "(?i)<Data Name ='IpAddress'>(::[\\w]+:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?"
      "(?i)<Data Name ='TicketEncryptionType'>({ticket_encryption_type}[^<]+)</Data>"
      "(?i)<Data Name ='TicketOptions'>({ticket_options}[^<]+)</Data>"
      "(?i)<Data Name ='ServiceName'>({service_name}[^<]+)</Data>"
      "(?i)\"Activity\":\"({event_name}[^\"]+)"
    ]
    ParserVersion = "v1.0.0"
  

}
```