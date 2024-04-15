#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-file-5058-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>5058<"
      "subjectlogonid'>"
    ]
    Fields = [
      "(?i)TimeCreated SystemTime(\\\\)?='({time}\\d+-\\d+-\\d+T\\d+:\\d+:\\d+)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)<Data Name[^<>]+?SubjectUserSid[^<>]+?>({user_sid}[^<>]+?)</Data>"
      "(?i)<Data Name[^<>]+?SubjectUserName[^<>]+?>({user}[^<>]+?)</Data>"
      "(?i)<Data Name[^<>]+?SubjectDomainName[^<>]+?>({domain}[^<>]+?)</Data>"
      "(?i)<Data Name[^<>]+?SubjectLogonId[^<>]+?>({login_id}[^<>]+?)</Data>"
      "(?i)<Data Name(\\\\)?='Operation'>({operation}[^<]+)"
      "(?i)<Data Name(\\\\)?='ReturnCode'>({return_code}[^<]+)"
      "(?i)<Data Name(\\\\)?='KeyName'>({key_name}[^<]+)"
      "(?i)<Data Name(\\\\)?='KeyType'>({key_type}[^<]+)"
    ]
    DupFields = [
      "host-> dest_host"
    ]
  

}
```