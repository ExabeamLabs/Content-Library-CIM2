#### Parser Content
```Java
{
Name = "microsoft-evnps-xml-radius-traffic-success-6272-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - NPS"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>6272<"
      "'subjectusername'>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d+-\\d+-\\d+T\\d+:\\d+:\\d+)"
      "(?i)<Computer>({host}[\\w\\-.]+)"
      "(?i)({event_code}6272)"
      "(?i)<EventRecordID>({event_id}[^<]+)"
      "(?i)'SubjectUserSid'>({user_sid}[^\"\\s<]+)<"
      "(?i)'SubjectUserName'>(?:({user_type}host)/)?(({domain}[^\\\\\\s\"<]+)\\\\+)?({user}[^\"\\\\\\s<]+)<"
      "(?i)'SubjectDomainName'>({domain}[^\"\\s<]+)<"
      "(?i)'NASIdentifier'>(?:-|({location}[\\w\\-.]+))"
      "(?i)'CallingStationID'>(?:-|({src_mac}[^\\<]+))"
      "(?i)'AuthenticationProvider'>(?:-|({auth_server}[^\\<]+))"
      "(?i)'FullyQualifiedSubjectMachineName'>(?:-|({user_type}.+?))(\\/[^\\/\\s]+)?<"
      "(?i)'NASIPv6Address'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?"
      "(?i)'NASIPv4Address'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?"
      "(?i)'EAPType'>(?:-|({auth_type}[^\\<]+))"
      "(?i)'QuarantineState'>(?:-|({access_type}[^\\<]+))"
    ]
    ParserVersion = "v1.0.0"
  

}
```