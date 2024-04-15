#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-create-success-4720-2-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4720</eventid>"
      "<data name='targetsid'>"
      "<message>a user account was created"
    ]
    Fields = [
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)<"
      "(?i)({event_code}4720)"
      "(?i)<Data Name ='TargetSid'>(?:NONE_MAPPED|({account_id}[^<]+))<"
      "(?i)<Data Name ='TargetUserName'>({account_name}[^<]+)<"
      "(?i)<Data Name ='TargetDomainName'>({account_domain}[^<]+)<"
      "(?i)<Data Name ='SubjectUserSid'>(?:NONE_MAPPED|({user_sid}[^<]+))<"
      "(?i)<Data Name ='SubjectUserName'>({user}[^<]+)<"
      "(?i)<Data Name ='SubjectDomainName'>({domain}[^<]+)<"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+)<"
      "(?i)({event_name}A user account was created)"
    ]
    DupFields = [
      "host->dest_host"
      "account_name->dest_user"
    ]
  

}
```