#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-modify-success-4738-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4738<"
    ]
    Fields = [
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Message>({event_name}A user account was changed)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Data Name ='SubjectUserSid'>({user_sid}[^<]+)"
      "(?i)<Data Name ='SubjectUserName'>({user}[^<]+)"
      "(?i)<Data Name ='SubjectDomainName'>({domain}[^<]+)"
      "(?i)<Data Name ='TargetUserName'>({dest_user}[^<]+)"
      "(?i)<Data Name ='TargetDomainName'>({dest_domain}[^<]+)"
      "(?i)<Data Name ='TargetSid'>({dest_user_sid}[^<]+)"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+)"
      "(?i)<Data Name ='OldUacValue'>({old_attribute}[^<]+)"
      "(?i)<Data Name ='NewUacValue'>({new_attribute}[^<]+)"
      "(?i)Changed Attributes:\\s*(|({attribute}[^:]+?))\\s+SAM Account Name:"
      "(?i)User Account Control:\\s*(-|({uac_status}[^:]+?))\\s*User Parameters:"
    ]
    ParserVersion = "v1.0.0"
  

}
```