#### Parser Content
```Java
{
Name = "microsoft-nps-xml-endpoint-authentication-success-6272-tl"
    Vendor = "Microsoft"
    Product = "Microsoft Network Policy Server"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>6272</eventid>"
      "<message>network policy server granted access to a user"
    ]
    Fields = [
      "(?i)SystemTime='({time}\\d\\d\\d\\d\\-\\d\\d\\-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[\\w\\-.]+)"
      "(?i)({event_code}6272)"
      "(?i)'SubjectUserName'>(?:({user_type}host)/)?(({domain}[^\\\\]+)\\\\+)?({user}[^<]+)"
      "(?i)'SubjectDomainName'>(?:-|({domain}[^\\s\\<]+))"
      "(?i)'FullyQualifiedSubjectUserName'>(({domain}[^\\\\]+)\\\\+)?(?:-|({user}[^\\s\\\\\\<]+))"
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