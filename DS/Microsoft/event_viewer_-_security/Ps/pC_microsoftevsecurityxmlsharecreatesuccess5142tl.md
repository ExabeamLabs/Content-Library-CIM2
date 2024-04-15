#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-share-create-success-5142-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "microsoft windows"
      "a network share object was added"
      "provider name='microsoft-windows-security-auditing"
      "<eventid>5142</eventid>"
    ]
    Fields = [
      "(?i)<TimeCreated\\s{1,100}SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d.\\d{1,100}Z)"
      "(?i)<Computer>({host}[^<]+)<\\/Computer>"
      "(?i)<Data\\sName ='SubjectDomainName'>({domain}[^<]+)"
      "(?i)<Data\\sName ='SubjectUserName'>({user}[^<]+)\\$"
      "(?i)<Data\\sName ='SubjectLogonId'>({login_id}[^<]+)"
      "(?i)<EventID>({event_code}[^<]+)"
      "(?i)<Data\\sName ='ShareName'>\\\\\\\\\\*\\\\({share_name}[^<]+)"
      "(?i)<Data\\sName ='ShareLocalPath'>({share_path}[^<]+)"
      "(?i)<Keyword>({result}[^<]+)<\\/Keyword>"
      "(?i)({event_name}a network share object was added)"
    ]
    DupFields = [
      "host->dest_host"
    ]
  

}
```