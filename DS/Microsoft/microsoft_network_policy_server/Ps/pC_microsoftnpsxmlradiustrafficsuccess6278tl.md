#### Parser Content
```Java
{
Name = "microsoft-nps-xml-radius-traffic-success-6278-tl"
    Vendor = "Microsoft"
    Product = "Microsoft Network Policy Server"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>6278</eventid>"
      "<message>network policy server granted full access to a user"
    ]
    Fields = [
      "(?i)SystemTime='({time}\\d\\d\\d\\d\\-\\d\\d\\-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[\\w\\-.]+)"
      "(?i)({event_code}6278)"
      """(?i)'SubjectUserName'>((?:host\/)({src_host}[^<]+)|({email_address}[^@<]+@[^<]+)|(({domain}[^\\<]+)\\+)?({user}[^<]+))"""
      "(?i)'SubjectDomainName'>(?:-|({domain}[^\\s\\<]+))"
      """(?i)'FullyQualifiedSubjectUserName'>([^<]+(\/|\\)(-|(({full_name}({first_name}[^\s<,]+),?\s({last_name}[^<]+))|({=user}[^<\s]+)))|(({domain}[^\\<]+)\\+)?(?:-|({=user}[^\s\\\<\/]+)))"""
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