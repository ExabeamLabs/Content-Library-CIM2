#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-share-delete-success-5144-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
    Conditions = [
      "<eventid>5144</eventid>"
      "microsoft-windows-security-auditing"
      "<data name="
      "a network share object was deleted"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime=('|\")({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)"
      "(?i)({event_name}A network share object was deleted)"
      "(?i)<Computer>({host}({dest_host}[\\w\\-]+)[^<]*)</Computer>"
      "(?i)<EventID>({event_code}5144)</EventID>"
      "(?i)<Data Name ='ShareName'>[\\\\*]+({share_name}[^<]+)<\\/Data>"
      "(?i)<Data Name ='SubjectDomainName'>({domain}[^<]+)<\\/Data>"
      "(?i)<Data Name ='ShareLocalPath'>({share_path}[^<]+)<\\/Data>"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+)<\\/Data>"
      "(?i)<Keyword>({result}[^<]+)<\\/Keyword>"
      "(?i)<Data Name ='SubjectUserName'>({user}[^<]+)<\\/Data>"
    ]
  

}
```