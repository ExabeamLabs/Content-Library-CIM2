#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-handle-request-4656-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>4656</eventid>"
      "subjectusersid"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime(\\\\)?=('|\")({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z('|\")\\/>"
      "(?i)<Computer>([^<>]+?[\\\\\\/]+)?({host}[^<>]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)<Data Name(\\\\)?=('|\")SubjectUserSid('|\")>({user_sid}[^<>]+)<"
      "(?i)<Data Name(\\\\)?=('|\")SubjectDomainName('|\")>(NT AUTHORITY|({domain}[^<>]+))<"
      "(?i)<Data Name(\\\\)?=('|\")SubjectUserName('|\")>(SYSTEM|({user}[^<>]+))<"
      "(?i)<Data Name(\\\\)?=('|\")ObjectServer('|\")>({object_server}[^<>]+)<"
      "(?i)<Data Name(\\\\)?=('|\")ObjectType('|\")>({object_class}[^<>]+)<"
      "(?i)<Data Name(\\\\)?=('|\")ObjectName('|\")>({object}[^<>]+)<"
      "(?i)<Data Name(\\\\)?=('|\")(HandleID|HandleId)('|\")>({object_id}[^<>]+)<"
      "(?i)<Data Name(\\\\)?=('|\")DesiredAccess('|\")>\\s*({access}[^<>]+)\\s*<"
      "(?i)<Data Name(\\\\)?=('|\")ProcessName('|\")>\\s*({process_path}({process_dir}(?:[^<]+)?[\\\\\\/]+)?({process_name}[^\\\\\\/\"<]+?))\\s*</Data>"
      "(?i)<Message>({event_name}[^\\.]+)"
      "(?i)<Data Name(\\\\)?='SubjectLogonId'>({login_id}[^<]+)"
      "(?i)<Keywords>({result}[^<]+)<"
    ]
  

}
```