#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-modify-success-5136-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>5136</eventid>"
      "<event xmlns='"
    ]
    Fields = [
      "(?i)<Computer>({host}({dest_host}[\\w-]+)[^<]*)</Computer>"
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d*Z'/>"
      "(?i)<Data Name ='SubjectLogonId'>\\s*({login_id}[^<]+?)\\s*</Data>"
      "(?i)<Data Name ='SubjectUserName'>\\s*(SYSTEM|({user}[^<]+?))\\s*</Data>"
      "(?i)<Data Name ='SubjectDomainName'>\\s*({domain}[^<]+?)\\s*</Data>"
      "(?i)<Data Name ='AttributeLDAPDisplayName'>\\s*({attribute}[^<]+?)\\s*</Data>"
      "(?i)<Data Name ='ObjectClass'>\\s*({ds_object_class}[^<]+?)\\s*</Data>"
      "(?i)<Data Name ='ObjectDN'>\\s*({object_dn}[^<]+?)\\s*</Data>"
      "(?i)({event_code}5136)"
      "(?i)<Message>({event_name}A directory service object was modified)"
    ]
    ParserVersion = "v1.0.0"
  

}
```