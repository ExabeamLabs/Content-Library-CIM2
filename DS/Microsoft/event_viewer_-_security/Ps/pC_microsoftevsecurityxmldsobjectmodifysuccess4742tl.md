#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-modify-success-4742-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>4742</eventid>"
      "<data name='targetsid'>"
      "<data name='targetusername'>"
      "<message>a computer account was changed"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)"
      "(?i)<Message>({event_name}A computer account was changed)"
      "(?i)<Computer>({host}[\\w\\-.]+)<"
      "(?i)<EventID>({event_code}4742)<"
      "(?i)<Data Name ='TargetUserName'>({dest_user}[^<]+)<"
      "(?i)<Data Name ='TargetDomainName'>({object_dn}[^<]+)<"
      "(?i)<Data Name ='SubjectUserName'>({user}[^<]+)<"
      "(?i)<Data Name ='SubjectDomainName'>({domain}[^<]+)<"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+)<"
      "(?i)<Data Name ='UserPrincipalName'>(-|({attribute}[^<]+))<"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```