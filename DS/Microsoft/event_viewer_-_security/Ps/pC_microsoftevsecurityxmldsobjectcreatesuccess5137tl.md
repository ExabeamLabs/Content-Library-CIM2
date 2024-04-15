#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-create-success-5137-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>5137</eventid>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)({event_code}5137)"
      "(?i)<Computer>({host}[\\w\\-\\.]+)</Computer>"
      "(?i)<Keywords>({result}[^<]+)</Keywords>"
      "(?i)<Data Name ='SubjectUserSid'>(|({user_sid}[^<]+?))</Data>"
      "(?i)<Data Name ='SubjectUserName'>(|({user}[^<]+?))</Data>"
      "(?i)<Data Name ='SubjectDomainName'>(|({domain}[^<]+?))</Data>"
      "(?i)<Data Name ='SubjectLogonId'>(|({login_id}[^<]+?))</Data>"
      "(?i)<Data Name ='ObjectDN'>(|({object_dn}[^<]+?))</Data>"
      "(?i)<Data Name ='ObjectClass'>(|({ds_object_class}[^<]+?))</Data>"
      "(?i)({event_name}A directory service object was created)"
    ]
    ParserVersion = "v1.0.0"
  

}
```