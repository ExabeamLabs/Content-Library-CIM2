#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-audit-policy-modify-success-4719-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4719<"
      "<data name='subjectusername'>"
    ]
    Fields = [
      "(?i)({event_code}4719)"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Computer>(\\d{1,3}.\\d{1,3}.\\d{1,3}.\\d{1,3}|({dest_host}[^<]+))"
      "(?i)<Data Name ='SubjectUserSid'>({user_sid}[^<]+)"
      "(?i)<Data Name ='SubjectUserName'>({user}[^<]+)"
      "(?i)<Data Name ='SubjectDomainName'>({domain}[^<]+)"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+)"
      "(?i)<Data Name ='CategoryId'>({category_id}[^<]+)"
      "(?i)<Data Name ='SubcategoryId'>({sub_category_id}[^<]+)"
      "(?i)<Data Name ='AuditPolicyChanges'>({audit_policy_name}[^<]+)"
      "(?i)<Message>({event_name}System audit policy was changed)"
    ]
    ParserVersion = "v1.0.0"
  

}
```