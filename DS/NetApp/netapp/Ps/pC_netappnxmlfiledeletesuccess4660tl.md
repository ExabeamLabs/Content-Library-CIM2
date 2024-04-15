#### Parser Content
```Java
{
Name = "netapp-n-xml-file-delete-success-4660-tl"
    Vendor = "NetApp"
    Product = "NetApp"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4660</eventid>"
      "subjectusersid"
      "netapp-security-auditing"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime=\"+({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>([^<>]+?[\\\\\\/]+)?({host}[^<>]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)<EventName>({event_name}[^<]+)<\\/EventName>"
      "(?i)<Result>({result}[^<]+)</Result>"
      "(?i)<Data Name =\"*SubjectIP\"*.*?>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?</Data>"
      "(?i)<Data Name =\"*SubjectUserSid\"*>({user_sid}.+?)</Data>"
      "(?i)<Data Name =\"*SubjectDomainName\"*>({domain}.+?)</Data>"
      "(?i)<Data Name =\"*SubjectUserName\"*>({user}.+?)</Data>"
      "(?i)<Data Name =\"*ObjectServer\"*>({object_server}.+?)</Data>"
      "(?i)<Data Name =\"*ObjectType\"*>({file_type}.+?)</Data>"
      "(?i)<Data Name =\"*ObjectName\"*>({file_path}.+?)<\\/Data>"
      "(?i)<Data Name =\"*ObjectName\"*>[^<]+[\\\\\\/]+({file_name}(?:[^<\\\\\\/:]+?)(\\.({file_ext}\\w+))?|[^\\\\:<]+)</Data>"
      "(?i)<Data Name =\"*ObjectName\"*>({file_dir}.+?)[\\\\\\/]+(?:[^\\\\\\/]+?)</Data>"
      "(?i)<Data Name =\"*ProcessName\"*>({process_path}({process_dir}(?:[^<]+)?[\\\\\\/])?({process_name}[^\\\\\\/\"<]+?))</Data>"
      "(?i)<Data Name =\"*(HandleID|HandleId)\"*>({object_id}.+?)</Data>"
    ]
    DupFields = [
      "event_name->operation"
    ]
    ParserVersion = "v1.0.0"
  

}
```