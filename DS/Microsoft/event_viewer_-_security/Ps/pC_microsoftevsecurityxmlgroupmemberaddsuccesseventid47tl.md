#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-group-member-add-success-eventid47-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>47"
      ">a member was added to a security-enabled"
      "<provider name="
    ]
    Fields = [
      "(?i)({event_name}A member was added to a security-enabled [\\w\\s]+ group)"
      "(?i)<TimeCreated SystemTime='({time}\\d+-\\d+-\\d+T\\d+:\\d+:\\d+.\\d+Z)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)A member was added to a security-enabled ({group_type}[^\\s]+) group"
      "(?i)<Data Name ='SubjectUserSid'>({user_sid}[^<]+)<"
      "(?i)<Data Name ='SubjectUserName'>({user}[^<]+)<"
      "(?i)<Data Name ='SubjectDomainName'>({domain}[^<]+)<"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+)<"
      "(?i)<Data Name ='MemberSid'>({account_id}[^<]+)<"
      "(?i)<Data Name ='TargetDomainName'>({group_domain}[^<]+)<"
      "(?i)<Data Name ='TargetSid'>({group_id}[^<]+)<"
      "(?i)<Data Name ='TargetUserName'>({group_name}[^<]+)<"
      "(?i)Member:(.+?({user_dn}CN=.+?,({user_ou}OU.+?DC=[\\w-]+))|(?:.+?))\\s*Group:"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```