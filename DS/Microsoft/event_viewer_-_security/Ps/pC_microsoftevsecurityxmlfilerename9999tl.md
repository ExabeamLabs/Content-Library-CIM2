#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-file-rename-9999-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>9999</eventid>"
      "subjectusersid"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime=('|\")({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z('|\")\\/>"
      "(?i)<Computer>([^<>]+?[\\\\\\/]+)?({host}[^<>]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)<Result>({result}[^<]+)</Result>"
      "(?i)<Data Name =('|\")SubjectIP('|\").*?>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?</Data>"
      "(?i)<Data Name =('|\")SubjectUserSid('|\")>({user_sid}.+?)</Data>"
      "(?i)<Data Name =('|\")SubjectDomainName('|\")>({domain}.+?)</Data>"
      "(?i)<Data Name =('|\")SubjectUserName('|\")>({user}.+?)</Data>"
      "(?i)<Data Name =('|\")ObjectServer('|\")>({object_server}.+?)</Data>"
      "(?i)<Data Name =('|\")NewPath('|\")>({file_path}({file_dir}.*?[\\\\\\/]+)?({file_name}[^\\\\\\/]+?(\\.({file_ext}\\w+))?))</Data>"
    ]
  

}
```