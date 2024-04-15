#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-group-member-remove-success-eventid-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "security id:"
      "logon id:"
      "a member was removed from a security-enabled"
      "<eventid>"
    ]
    Fields = [
      "(?i)({event_name}A member was removed from a security-enabled [\\w\\s]+ group)"
      "(?i)SystemTime(\\\\)?='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d.\\d\\d\\d)\\d+Z'"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<EventID>({event_code}[^<]+)"
      "(?i)A member was removed from a security-enabled\\s*({group_type}[^\\s]+)\\s+group"
      "(?i)'MemberName'>(-|({account_id}[^<]+))<"
      "(?i)'MemberSid'>({user_sid}[^<]+)"
      "(?i)'SubjectUserSid'>({user_sid}[^\"\\s<]+)<"
      "(?i)'SubjectUserName'>({user}[^\"\\s<]+)<"
      "(?i)'SubjectDomainName'>({domain}[^\"\\s<]+)<"
      "(?i)'SubjectLogonId'>({login_id}[^\"\\s<]+)<"
      "(?i)CN=({account_id}.*?(?=\\s*,OU))"     
      "(?i)OU=({user_ou}[^,]+)"
      "(?i)DC=({user_dn}[^,<]+)"
      "(?i)'TargetUserName'>({group_name}[^<]+)"
      "(?i)'TargetDomainName'>({group_domain}[^<]+)"
      "(?i)'TargetSid'>({group_id}[^<]+)"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```