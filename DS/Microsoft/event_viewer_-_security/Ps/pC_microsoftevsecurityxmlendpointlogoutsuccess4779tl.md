#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-logout-success-4779-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4779<"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime(\\\\)?='({time}\\d+-\\d+-\\d+T\\d+:\\d+:\\d+)"
      "(?i)<Computer>({host}[\\w\\-.]+)"
      "(?i)({event_code}4779)"
      "(?i)<Message>({event_name}[^.。]+)"
      "(?i)<EventRecordID>({event_id}[^<]+)"
      "(?i)'AccountName'>({user}[^\"\\s<]+)<"
      "(?i)'AccountDomain'>({domain}[^\"\\s<]+)<"
      "(?i)'LogonID'>({login_id}[^\"\\s<]+)<"
      "(?i)'ClientName'>({src_host}[\\w\\-.]+)<"
      "(?i)'ClientAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?<"
      "(?i)<Keywords>({result}[^<]+)</Keywords>"
    ]
  

}
```