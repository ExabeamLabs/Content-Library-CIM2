#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-link-create-4664-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>4664<"
      "an attempt was made to create a hard link"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)"
      "(?i)<Computer>({host}[^<>]+)<\\/Computer>"
      "(?i)<Message>({event_name}[^:<\\.]+)"
      "(?i)<Message>({event_name}[^<]+?)\\.(\\s|<)"
      "(?i)'SubjectUserSid'>({user_sid}[^'<\\s]+)<"
      "(?i)'SubjectUserName'>({user}[^'<\\s]+)<"
      "(?i)'SubjectDomainName'>({domain}[^'<\\s]+)<"
      "(?i)'SubjectLogonId'>({login_id}[^'<\\s]+)<"
      "(?i)'FileName'>(|({file_path}({file_dir}[^\"<]*?)[\\\\\\/]*({file_name}[^\\\\\\/\"<]+?(\\.({file_ext}[^\\\\\\/\\.\\s\"<]+))?)))<"
      "(?i)'TransactionId'>\\{?({transaction_id}[^'<\\}]+)\\}?<"
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)<Keyword>({result}.+?)</Keyword>"
    ]
  

}
```