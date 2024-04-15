#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-file-success-4663-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4663</eventid>"
      "<data name=\"subjectusersid\""
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime=\"({time}\\d+-\\d+-\\d+T\\d+:\\d+:\\d+)"
      "(?i)<Computer>([^<>]+?[\\\\\\/]+)?({host}[^<]+)</Computer>"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)<Data Name =\"SubjectUserSid\">(?:NONE_MAPPED|({user_sid}[^<]+))<"
      "(?i)<Data Name =\"SubjectUserName\">(?=\\w)({user}[^<]+)<"
      "(?i)<Data Name =\"SubjectDomainName\">(?=\\w)({domain}[^<]+)<"
      "(?i)<Data Name =\"SubjectLogonId\">({login_id}[^<]+)<"
      "(?i)<Data Name =\"ObjectType\">({file_type}[^<]+)<"
      "(?i)<Data Name =\"ObjectName\">({src_file_path}[^<]+)<"
      "(?i)<Data Name =\"ObjectName\">[^<]+[\\\\\\/]+({src_file_name}(?:[^<\\\\\\/:]+?)(\\.({src_file_ext}\\w+))?|[^\\\\:<]+)<"
      "(?i)<Data Name =\"ObjectName\">({file_dir}.+?)[\\\\\\/]+(?:[^\\\\\\/]+?)<"
      "(?i)<Data Name =\"ProcessName\">({process_path}({process_dir}(?:[^<]+)?[\\\\\\/])?({process_name}[^\\\\\\/\\\"<]+?))<"
      "(?i)<Data Name =\"AccessList\">([^\\d\\w]+)?({access}[\\d\\w]+)"
      "(?i)<Data Name =\"AccessMask\">({access_mask}[^<]+)"
      "(?i)Accesses:\\s*({access}[^:]+?)\\s*Access Mask:"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```