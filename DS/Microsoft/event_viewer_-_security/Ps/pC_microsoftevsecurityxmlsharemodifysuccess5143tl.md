#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-share-modify-success-5143-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>5143"
      ">a network share object was modified"
      "<data name='subjectusersid'"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)'"
      "(?i)<Computer>({host}[\\w\\-.]{1,20000})<"
      "(?i)<EventID>({event_code}5143)"
      "(?i)<Data Name ='SubjectUserSid'>({user_sid}[^<]+)<"
      "(?i)<Data Name ='SubjectUserName'>({user}[^<]+)<"
      "(?i)<Data Name ='SubjectDomainName'>({domain}[^<]+)<"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+)<"
      "(?i)<Data Name ='ObjectType'>({file_type}[^<]+)<"
      "(?i)<Data Name ='ShareName'>[\\\\\\*]*({share_name}[^<]+)<"
      "(?i)<Data Name ='ShareLocalPath'>[\\\\\\?]*({share_path}(({d_parent}[^@]+?)\\\\)?(|({d_name}[^\\\\]+?)))<"
      "(?i)<Message>({event_name}A network share object was modified)"
    ]
  

}
```