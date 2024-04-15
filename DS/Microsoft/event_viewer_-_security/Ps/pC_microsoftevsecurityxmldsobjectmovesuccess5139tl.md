#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-move-success-5139-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>5139</eventid>"
      "<event xmlns='"
    ]
    Fields = [
      "(?i)<Computer>({host}.+?)</Computer>"
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z'/>"
      "(?i)<Data Name ='SubjectLogonId'>\\s*({login_id}.+?)\\s*</Data>"
      "(?i)<Data Name ='SubjectUserName'>\\s*(SYSTEM|({user}[^\\s]+?))\\s*</Data>"
      "(?i)<Data Name ='SubjectDomainName'>\\s*({domain}[^\\s]+?)\\s*</Data>"
      "(?i)<Data Name ='SubjectUserSid'>\\s*({user_sid}[^\\s]+?)\\s*</Data>"
      "(?i)<Data Name ='ObjectClass'>\\s*({ds_object_class}.+?)\\s*</Data>"
      "(?i)<Data Name ='NewObjectDN'>\\s*({src_ds_object_dn}.+?)</Data>\\s*"
      "(?i)({event_code}5139)"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```