#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-share-access-success-5140-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>5140</eventid>"
      "<data name"
      "'sharename'>"
    ]
    Fields = [
      "(?i)<EventID>({event_code}5140)"
      "(?i)<Computer>({host}({dest_host}[\\w-]+)[^<]*)</Computer>"
      "(?i)<TimeCreated SystemTime(\\\\\\/)?='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d*Z'/>"
      "(?i)<Data Name(\\\\\\/)?='SubjectLogonId'>({login_id}[^<]+?)</Data>"
      "(?i)<Data Name(\\\\\\/)?='SubjectUserName'>(-|({user}[^<]+?))</Data>"
      "(?i)<Data Name(\\\\\\/)?='SubjectDomainName'>({domain}[^<]+?)</Data>"
      "(?i)<Data Name(\\\\\\/)?='ObjectType'>({file_type}[^<]+?)</Data>"
      "(?i)<Data Name(\\\\\\/)?='IpAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?</Data>"
      "(?i)<Data Name(\\\\\\/)?='ShareName'>(?:[\\\\\\*]*)?({share_name}[^<]+?)</Data>"
      "(?i)<Data Name(\\\\\\/)?='ShareLocalPath'>(?:[\\\\\\\\/?]+)?(|({share_path}({d_parent}[^<]+?[\\\\\\/])?({d_name}[^\\\\\\/<]+?)?[\\\\\\/]?))</Data>"
      "(?i)({access}4416)"
      "(?i)<Data Name(\\\\\\/)?='AccessList'>(%%)?({access}[\\d\\w]+)"
    ]
    ParserVersion = "v1.0.0"
  

}
```