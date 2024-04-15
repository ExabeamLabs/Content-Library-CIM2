#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-share-access-5145-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>5145<"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d+-\\d+-\\d+T\\d+:\\d+:\\d+)"
      "(?i)<Computer>({host}[\\w\\-.]+)"
      "(?i)<Computer>(\\d{1,3}.\\d{1,3}.\\d{1,3}.\\d{1,3}|({host}[\\w\\-.]+))"
      "(?i)({event_code}5145)"
      "(?i)<EventRecordID>({event_id}[^<]+)"
      "(?i)'SubjectUserSid'>({user_sid}[^\"\\s<]+)<"
      "(?i)'SubjectUserName'>({user}[^\"\\s<]+)<"
      "(?i)'SubjectDomainName'>({domain}[^\"\\s<]+)<"
      "(?i)'SubjectLogonId'>({login_id}[^\"\\s<]+)<"
      "(?i)'ObjectType'>({file_type}[^<]+)<"
      "(?i)'IpAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?<"
      "(?i)'IpPort'>({src_port}\\d+)"
      "(?i)'ShareName'>(?:\\\\+\\*\\\\+)?({share_name}.+?)<\/Data>"
      "(?i)'ShareLocalPath'>(?:[\\\\\\?]+)?(?:\\s*|({share_path}({d_parent}[^<]*?)({d_name}[^\\\\<]+?)))<\/Data>"
      "(?i)'RelativeTargetName'>((|({f_parent}[^<]+?))({file_name}[^\\\\:<]+?(\\.({file_ext}[^\\\\.<]+?))?))<\/Data>"
      "(?i)'ObjectType'>({file_type}[^<]+)<"
      "(?i)'ObjectType'>({file_type}[^<]+)<"
    ]
    ParserVersion = "v1.0.0"
  

}
```