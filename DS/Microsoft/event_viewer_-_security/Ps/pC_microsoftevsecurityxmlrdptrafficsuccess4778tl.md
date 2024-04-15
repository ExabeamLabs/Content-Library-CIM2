#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-rdp-traffic-success-4778-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4778<"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime(\\\\)?='({time}\\d+-\\d+-\\d+T\\d+:\\d+:\\d+)"
      "(?i)<Computer>({host}[\\w\\-.]+)"
      "(?i)({event_name}A session was reconnected to a Window Station)"
      "(?i)({event_code}4778)"
      "(?i)<EventRecordID>({event_id}[^<]+)"
      "(?i)'AccountName'>({user}[^\"\\s<]+)<"
      "(?i)'AccountDomain'>({domain}[^\"\\s<]+)<"
      "(?i)'LogonID'>({login_id}[^\"\\s<]+)<"
      "(?i)'ClientName'>({src_host}[\\w\\-.]+)<"
      "(?i)'ClientAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?<"
    ]
    ParserVersion = "v1.0.0"
  

}
```