#### Parser Content
```Java
{
Name = "microsoft-nps-xml-radius-traffic-fail-6274-tl"
    Vendor = "Microsoft"
    Product = "Microsoft Network Policy Server"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>6274</eventid>"
      "<message>network policy server discarded the request for a user."
    ]
    Fields = [
      "(?i)SystemTime='({time}\\d\\d\\d\\d\\-\\d\\d\\-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[\\w\\-.]+)"
      "(?i)({event_code}6274)"
      """(?i)'SubjectUserName'>(?:({user_type}host)/)?(({domain}[^\\<]+)\\+)?(({email_address}[^@\s\\\<\/]+@[^@\s\\\<\/]+)|(({user}[\w-]+)(\.[\w.]+)?)|({full_name}[\w,-]+?))<"""
      "(?i)'SubjectDomainName'>(?:-|({domain}[^\\s\\<]+))"
      """(?i)'FullyQualifiedSubjectUserName'>(({domain}[^\\\/<]+)\\+)?(?:-|({email_address}[^@\s\\\<\/]+@[^@\s\\\<\/]+)|(({user}[\w-]+)(\.[\w.]+)?)|({full_name}[\w,-]+?))<"""
      """(?i)'FullyQualifiedSubjectUserName'>(({domain}[^\\\/<]+)\/+)?({user_group_name}[^\s\<\/]+)(\/([^\/]+))?\/(?:-|({email_address}[^@\s\\\<\/]+@[^@\s\\\<\/]+)|(({user}[\w-]+)(\.[\w.]+)?)|({full_name}[^\s\/<]+\s+[^\s<\/]+))<"""
      "(?i)'NASIdentifier'>(?:-|({location}[\\w\\-.]+))"
      "(?i)'AuthenticationProvider'>(?:-|({auth_server}[^\\<]+))"
      "(?i)'FullyQualifiedSubjectMachineName'>(?:-|({user_type}.+?))(\\/[^\\/\\s]+)?<"
      "(?i)'NASIPv6Address'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?"
      "(?i)'NASIPv4Address'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?"
      "(?i)'Reason'>({failure_reason}[^<]+)"
      "(?i)({result}discarded)"
    ]
    ParserVersion = "v1.0.0"
  

}
```