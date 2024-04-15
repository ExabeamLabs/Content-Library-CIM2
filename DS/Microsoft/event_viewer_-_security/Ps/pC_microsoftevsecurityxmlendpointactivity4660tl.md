#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-activity-4660-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>4660</eventid>"
      "subjectusersid"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime(\\\\)?=('|\")({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z('|\")\\/>"
      "(?i)<Computer>([^<>]+?[\\\\\\/]+)?({host}[^<>]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)<Data Name(\\\\)?=('|\")SubjectIP('|\").*?>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?</Data>"
      "(?i)<Data Name(\\\\)?=('|\")SubjectUserSid('|\")>({user_sid}.+?)</Data>"
      "(?i)<Data Name(\\\\)?=('|\")SubjectDomainName('|\")>({domain}.+?)</Data>"
      "(?i)<Data Name(\\\\)?=('|\")SubjectUserName('|\")>({user}.+?)</Data>"
      "(?i)<Data Name(\\\\)?=('|\")ObjectServer('|\")>({object_server}.+?)</Data>"
      "(?i)<Data Name(\\\\)?=('|\")ObjectType('|\")>({object_class}.+?)</Data>"
      "(?i)<Data Name(\\\\)?=('|\")ObjectName('|\")>({object}.+?)</Data>"
      "(?i)<Data Name(\\\\)?=('|\")(HandleID|HandleId)('|\")>({object_id}.+?)</Data>"
      "(?i)<Data Name =('|\")ProcessName('|\")>\\s*({process_path}({process_dir}[^\"<]+?)({process_name}[^\"<\\\\]+))\\s*</Data>"
      "(?i)<Data Name(\\\\)?='SubjectLogonId'>({login_id}[^<]+)"
      "(?i)<EventName>({event_name}[^<]+)<\\/EventName>"
    ]
  

}
```