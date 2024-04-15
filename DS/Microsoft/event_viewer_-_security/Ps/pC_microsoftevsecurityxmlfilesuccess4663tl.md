#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-file-success-4663-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4663</eventid>"
      "<data name='subjectusersid'"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d+-\\d+-\\d+T\\d+:\\d+:\\d+)"
      "(?i)<Computer>({host}[^<]+)<"
      "(?i)<EventID>({event_code}[^<]+)<"
      "(?i)<Data Name ='SubjectUserSid'>(?:NONE_MAPPED|({user_sid}[^<]+))<"
      "(?i)<Data Name ='SubjectUserName'>({user}[^<]+)<"
      "(?i)<Data Name ='SubjectDomainName'>({domain}[^<]+)<"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+)<"
      "(?i)<Data Name ='ObjectType'>({file_type}[^<]+)<"
      "(?i)<Data Name ='ObjectName'>({file_path}[^<]+)<"
      "(?i)<Data Name ='ObjectName'>[^<]+[\\\\\\/]+({file_name}(?:[^<\\\\\\/:]+?)(\\.({file_ext}\\w+))?|[^\\\\:<]+)<"
      "(?i)<Data Name ='ObjectName'>({file_dir}.+?)[\\\\\\/]+(?:[^\\\\\\/]+?)<"
      "(?i)<Data Name ='ProcessName'>({process_path}({process_dir}(?:[^<]+)?[\\\\\\/])?({process_name}[^\\\\\\/\\\"<]+?))<"
      "(?i)<Data Name ='AccessList'>([^\\d\\w]+)?({access}[\\d\\w]+)"
      "(?i)<Data Name ='AccessMask'>({access_mask}[^<]+)"
      "(?i)Accesses:\\s*({access}[^:]+?)\\s*Access Mask:"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```